# Quelques rappels sur jQuery

Avant de nous lancer dans le vif du sujet, il peut être intéressant de rappeler quelques éléments clés du Framework jQuery. En effet, comme son nom le laisse suggérer et comme nous l'avons souligné en début d'ouvrage, jQuery Mobile est basé sur la célèbre librairie JavaScript. Nous allons donc dans cette partie refaire le tour des principales fonctions et astuces de la librairie qui nous serons utiles dans l'utilisation de jQuery Mobile.

## 2.1 . Sélection d'éléments

La sélection d'éléments en jQuery se fait à l'aide du tag raccourci $\(\), qui est en fait l'équivalent du sélecteur jQuery\(\). Il prend en paramètre l’élément recherché. En voici la syntaxe :

```js
<script>
jQuery('l_element_a_selectionne');

//Ou en plus simple...
$('l_element_a_selectionne');

</script>
```

### Exemples de sélections  intéressantes:

#### Sélectionne tous les éléments de la page \(DOM\)

```js
$("*") ;
```

#### Sélection d’éléments HTML

* Paragraphe :

  * ```js
    $('p') ; //Sélectionne tous les paragraphes de la page html
    ```

* Sélection tous les éléments de type hx \(h1, h2, h3, h4, ...\)

  * ```js
    $(":header") ;
    ```

* Liste à puces :

  * ```js
    $('li') ; //Sélectionne tous les éléments de type liste.
    ```

#### Sélection de classes css et d'id

```js
$('.demo') ; //La classe s’appelle ‘demo’


$('#contenu') ; //L’id s’appelle ‘contenu’
```

#### Sélectionne d'éléments comportant un mot clé

```js
$(":contains('mobinaute')") ; // Renvoie tous les éléments contenant le mot clé "mobinaute"
```

#### Sélection d'éléments HTML

```
$("a:has(img)") ; // Renvoi tous les blocs d'éléments comportant des images
```

```
$(input[type= "submit"]) ou $( :submit); // Sélectionne tous les éléments de type submit
```

```
$("td:empty") ; // Sélectionne toutes les cases vides d 'un tableau
```

Une fois ces éléments sélectionnés on peut leur appliquer un certain nombre de changements gérés dynamiquement par jQuery.

Ainsi si nous souhaitons ajouter une classe **'rouge'** à un élément ayant pour id le mot header et une classe 'noir' à un élément ayant pour id le mot footer, il suffira d'écrire :

```js
$(document).ready( function() {

    $('#header').addClass('rouge');

    $('#footer').addClass('noir');

});
```

La fonction **$\(\)** va donc nous permettre de sélectionner tout \(ou presque tout\) ce que l'on souhaite.

## 2.2 . Manipulation du DOM1 \(Document Object Model\)

La manipulation du DOM[^1] est l'étape qui suit généralement la sélection. L'idée est donc de récupérer un éléments du DOM, puis de lui affecter un certain nombre de propriétés. Il existe de nombreuses fonctions jQuery facilitant la manipulation du DOM. Mais nous nous intéresserons qu'à un certain nombre d'entre eux, que nous pensons être les plus importants quand il s'agit de développer avec jQuery Mobile.

### 2.2.1 La fonction text\(\)

Supposons que nous ayons le code html suivant :

```js
<html>

<body>

<div class="container">

    <h1 id="titre">Demo1 jQuery - Manipulation du DOM</h1> 
    <p id="contenu">

        Hello <b>Mobinaute</b> <br />

        Je suis un contenu qui va s'afficher sous forme d'alerte. <br /> 
        Je suis un exemple pour montrer à quel point il est facile d'utiliser la fonction 
        <strong>text()</strong>.
    </p>

</div>

</body>

</html>
```

Il est très facile de récupérer le contenu du paragraphe ayant l'id **'contenu'** grâce à la fonction text\(\) :

```js
var contenu = $("#contenu").text();
```

La variable contenu contient le texte du paragraphe.

Dans cet exemple, nous affichons simplement le contenu du paragraphe dans une alerte javascript :

```js
<script>

var contenu = $('#contenu').text(); // Juste du texte

alert('## DEBUT ## ' + contenu + ' ## FIN ##');// Affiche une alerte </script>
```

![](/assets/jqm_exemple_1.jpeg.jpg)

Si l'on souhaite à présent changer le contenu du paragraphe, il suffit de faire :

```
$("#contenu").text("Bonjour le Monde");
```

Qui a pour effet de remplacer le contenu actuel du paragraphe par **« Bonjour le Monde »** .

De façon générale, La fonction text\(\) sans argument permet de récupérer le contenu d'un élément du DOM, tandis qu'avec un argument de type chaîne de caractère, celle-ci va remplacer le contenu courant par celui indiqué en paramètre.

![](/assets/jqm_exemple_2.jpeg.jpg)

### 2.2.2 La fonction html\(\)

La fonction **html\(\)** permet de récupérer tout le contenu d'un élément \(aussi bien du texte que des balises html\).

Pour la voir en action, modifions un peu le code html précédent :

```js
<html>
    ...
    <body>
    
        <div class="container">
            
            <h1 id="titre">Demo2 jQuery - Manipulation du DOM</h1> 
            <div id="contenu1">                
                <p>
                    Voici du beau contenu html qui sera entièrement récupéré.
                </p>
                
                <ul>
                    <li>1 - Un</li>                    
                    <li>2 - Deux</li>
                </ul>            
            </div><!--- Contenu html qui sera récupéré-->
        
        </div><!--- Container -->
    
    </body >

</html >
```



Pour récupérer le contenu HTML, il suffit de faire :

```js
var contenuHTML = $("#contenu2").html();
```

La variable _**contenuHTML**_ contient le code html qui se trouve à l’intérieur de la div **\(id='contenu'\)**.

![](/assets/jqm_exemple_3.jpg)

Si l'on souhaite par contre modifier le contenu du bloc en y insérant autre chose , il suffit de faire :

```js
$('#secondaire').html(autre_contenuHTML);
```

Insertion d'un nouveau contenu html

```js
<script>

var autre_contenuHTML = "<p>Voici un nouveau contenu qui montrer la facilité d'utilisation de la fonction <b>html()</b><p>";

var contenuHTML = $('#contenu').html(autre_contenuHTML); alert('## DEBUT ## ' + contenuHTML + ' ## FIN ## ');

</script>
```

### 2.2.3 La fonction remove

Supprime tous les éléments du DOM répondant aux critères de sélection. Attention, cette fonctionne ne supprime PAS les éléments de l'objet jQuery, ce qui permet une utilisation de ces éléments même si ceux ci ne figurent plus dans le document.



Considérons le contenu html suivant :

```js
<div class="container">


<div class="hello">Hello</div>

<div class="world">World</div>


</div>
```



Nous choisissons de supprimer le mot 'World' du contenu. Il suffit de faire :

```js
$('.hello').remove();
```

Qui aura pour résultat la suppression du bloc contenant la classe 'world'. On aura finalement :



```js
<div class="container">


<div class="world">World</div>


</div>
```



Si plusieurs blocs possèdent la classe sélectionnée, ils seront également supprimer. Cette fonction est particulièrement intéressante dans le cas où l'on souhaiterait supprimer du contenu, sans affecter la hiérarchie du DOM.

### 2.2.4 Autre exemple : Suppression de tous les paragraphes du DOM

```js
<!DOCTYPE html>

<html>

<head>
    <script src="http://code.jquery.com/jquery-latest.js"></script> <style>p { background:blue; }</style> 
</head>

<body>

<p>Hello mobinaute ! </p>

<p>Comment vas-tu</p>

Ce texte ne sera PAS supprimé.

<p>aujourd'hui?</p>

<button>Supprimer les paragraphes</button>

<script>
    $("button").click(function () {
    
        $("p").remove();
    
    });
</script>

</body>

</html>
```

On peut aussi choisir de ne supprimer que des paragraphes possédant une certaine classe.

```js
<!DOCTYPE html>

<html>

<head>

<style>p { background:blue; }</style>

<script src="http://code.jquery.com/jquery-latest.js"></script> </head>

<body>

    <p class="hello">Hello mobinaute ! </p>
    
    <p>Comment vas-tu</p>
    
    Ce texte ne sera PAS supprimé.
    
    <p>aujourd'hui?</p>
    
    <button>Supprimer les paragraphes</button>
    
    <script>
        $("button").click(function () {
        
        $("p").remove(":contains('Hello')");
        
        });
    </script>

</body>
</html>
```

## 2.3 . Gestion des événements

Les événements font partis intégrante de jQuery. Ils permettent de gérer les actions utilisateurs, comme le clic sur un bouton. Voici 2 d’événements très utilisés :

* **document.ready\(\)** permet de déclencher l’exécution du code au chargement complet de la page en cours, ceci remplace la fonction onload\(\) de JavaScript.



* **click** :
  * ```js
    // L'exemple ci-dessous permet de simuler le clic d'un utilisateur.
    $('#mon_selecteur').click( function() {
        // Un code Javascript
    });

    ...
    <!-- Mon code html -->
    <button id="mon_selecteur">Cliquez-moi</button>
    ```



D'autres événements se fondent sur le même principe : blur, bind, change, mouseon, mouseup …

Dans les exemple précédents, nous avons sans le signaler utilisé des événements. Il en existe un certain nombre, plusieurs dizaines pris en charges par jQuery, mais les plus utilisés sont très certainement bind, click, toggle, change, submit , ready et load. Un événement est presque toujours associé à une sélection, et donc affecté à un objet du DOM.

[^1]: Le DOM \(Document Object Model\) est une interface de programmation \(API\) qui décrit la structure d'un document et surtout la manière d'y accéder et de le manipuler. Plus d'informations sur Wikipédia \([http://fr.wikipedia.org/wiki/Document\_Object\_Model\](http://fr.wikipedia.org/wiki/Document_Object_Model%29\)

