# 1 . Introduction au Framework

## 1.1 . jQuery au cœur de l'internet Mobile

Pour le dire de façon sommaire, jQuery Mobile est une outil logiciel qui fonctionne de manière transparente sur toutes les plate-formes mobiles du moment. Aussi riche que sa parente jQuery, dont la renommée n'est plus à faire auprès des développeurs web, jQuery Mobile est la bibliothèque JavaScript la plus adaptée pour créer des sites web à destination des smartphones et tablettes tactiles.

Avec ses presque 1,2 Milliards d'utilisateurs, soit environ 17 % de la population mondiale, l'internet mobile continu de croître de façon considérable. On estime, grâce à un sondage de Médiamétrie, qu'en 2012 la moitié de la population française y sera connectée. La grande diversités des écrans de terminaux mobiles est devenue un véritable casse-tête pour les développeurs de sites web mobiles, soucieux de ne pas rater le passage à l'ère du tout mobile.

Grâce à jQuery Mobile, il est désormais facile de créer des sites et applications web performantes, qui s'adaptent à tous les types d'interfaces. Aujourd'hui en version 1.0, jQuery Mobile est déjà déclarée "Innovation de l'année" par les .Net Awards ! Qu'il s'agisse des fenêtres et composants graphiques d'interface HTML/CSS ou de l'interaction du site avec des données extérieures \[base de données sur un serveur distant, géolocalisation avec Google Maps...\) grâce à JavaScript, jQuery Mobile \(jQM\) donne tous les éléments pour construire, avec une agréable facilité, des sites qui fonctionneront sur la plupart des supports mobiles actuels.

L’explosion des ventes de smartphones et le besoin toujours plus grand des internautes d’être connecté au monde a favoriser la croissance de ce type de plates-formes de développement mobile. Pour de nombreux développeurs, jQuery Mobile est tout simplement en tête du classement. L'inclure dans ses projets est un donc choix absolument stratégique.

## 1.2 . Découvrir Le Framework

### 1.2.1 Installation de jQuery Mobile

Installer la plate-forme jQuery Mobile se fait aussi simplement que l'installation de jQuery. Il suffit en effet de soit :

* **Télécharger le fichier JavaScript et de l'appeler dans son fichier html**. Il faut dans ce cas télécharger également:
  * La feuille de style jquerymobile.css
  * Le dossier d'images à mettre dans le même répertoire que les fichiers.

* **Faire un lien vers les fichiers JavaScript et CSS** directement hébergés par les fondateurs du Framework. Cette méthode a l'avantage de nous éviter de télécharger des documents \(JavaScript, images\).

Étant donné que jQuery Mobile dépend du Framework jQuery, celui-ci doit être invoqué bien avant l'importation de jQM. Concrètement on aura avoir ceci :

```js
<!doctype html>
<html >
<head>
    <title>Ma première Page</title>
    <meta name="viewport" content="width=device-width, initial-scale=1"> 
    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.css" />
    <script src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
    <script src="http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.js"></script>
</head>
<body >
….
</body >
```

### 1.2.2 Une première application

Un template jQuery Mobile se définit très facilement. Il est presque toujours composé d'une ou plusieurs page, définies dans un document écrit en HTML 5 :

Une page contenant généralement :

* **Un titre** \(entête, header\)
* **Du contenu** \(content\)
* **Un pied de page** \(footer\)

Définition d'une page de base en jQuery Mobile :

```js
<body >
    <div data-role="page">
        <div data-role="header">
            <h1>Un Titre</h1>
        </div><!-- /header →
        
        <div data-role="content">
            <p>Hello world</p>
        </div><!-- /content -->
        
    </div><!-- /page -->
</body >
```

Et avec un exemple complet :

```js
<!doctype html>
<html >
<head>
    <title>Ma première Page</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.css" />
    <script src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
    <script src="http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.js"></script>
</head>
<body >
    <div data-role="page">
        <div data-role="header">
            <h1>Un Titre</h1>
        </div><!-- /header →
        
        <div data-role="content">
            <p>Bonjour le monde !</p>
        </div><!-- /content -->
        
    </div><!-- /page -->
</body >
```





Bravo, vous venez officielement de démarrer votre projet jQuery Mobile. Etonnant de simplicité n'est-ce pas ? Passons donc à la suite qui devrait vraiment vous plaire.

