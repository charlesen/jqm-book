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

        Je suis un contenu qui va s'afficher sous forme d'alerte. <br /> Je suis un exemple pour montrer à quel point il est facile d'utiliser la fonction <b>text()</b>.

    </p>

</div>

</body >

</html >
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

cd

[^1]: Le DOM \(Document Object Model\) est une interface de programmation \(API\) qui décrit la structure d'un document et surtout la manière d'y accéder et de le manipuler. Plus d'informations sur Wikipédia \([http://fr.wikipedia.org/wiki/Document\_Object\_Model\](http://fr.wikipedia.org/wiki/Document_Object_Model\)\)

