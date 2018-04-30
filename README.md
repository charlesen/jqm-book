# Développer avec jQuery Mobile {#d-velopper-avec-jquery-mobile}

![](export/assets/image1.png)![](export/assets/image2.png)

|  |  | **Développer avec jQuery Mobile – Première Édition** |
| --- | --- | --- |
|  |  |  |
|  |  |  |  |  |
| Table des matières |  |  |
|  |  |  |
| 1 .Introduction au Framework..................................................................................................... | 5 |
| 1.1 | . jQuery au cœur de l&#039;internet Mobile......... .......................................................................5 |  |
| 1.2 | . Découvrir Le Framework................................................................................................6 |  |
| 1.2.1 | Installation de jQuery Mobile.....................................................................................6 |  |
| 1.2.2 | Une première application..........................................................................................7 |  |
| 2 .Rappels sur jQuery.................................................................................................................9 |  |
| 2.1 | .Sélection d&#039;éléments......................................................................................................9 |  |
| 2.2 | .Manipulation du DOM (Document Object Model).......................................................... | 11 |  |
| 2.2.1 | La fonction text()..................................................................................................... | 11 |  |
| 2.2.2 | La fonction html().................................................................................................... | 13 |  |
| 2.2.3 | La fonction remove................................................................................................. | 15 |  |
| 2.3 | .Gestion des événements.............................................................................................. | 17 |  |
| 2.3.1 | L’événement bind................................................................................................... | 17 |  |
| 2.3.2 | L&#039;événement click.................................................................................................. | 18 |  |
| 2.3.3 | L&#039;événement toggle................................................................................................ | 20 |  |
| 2.3.4 | L&#039;événement submit............................................................................................... | 23 |  |
| 2.4 | .Ajouter des effets.......................................................................................................... | 23 |  |
| 2.4.1 hide() et show()....................................................................................................... | 23 |  |
| 2.5 | .Autres fonctions intéressantes....................................................................................... | 23 |  |
| 2.5.1 | $.browser................................................................................................................ | 23 |  |
| 2.5.2 each........................................................................................................................ | 24 |  |
| 2.5.3 after........................................................................................................................ | 24 |  |
| 2.6 | .Développer avec Ajax.................................................................................................... | 25 |  |
| 2.7 | .Travaux pratiques.......................................................................................................... | 27 |  |
| 3 . Utilisation des composants jQuery Mobile............................................................................ | 28 |  |
| 3.1 | .Créer une page avec jQuery Mobile.............................................................................. | 28 |  |
| 3.1.1 | Structure d&#039;une page............................................................................................... | 28 |  |
| 3.1.2 | Contenu d&#039;une page................................................................................................ | 29 |  |
| 3.1.3 | Structure multi-page................................................................................................ | 31 |  |
| 3.1.4 | Passage d&#039;une page à l&#039;autre................................................................................. | 34 |  |
| 3.1.5 | Utiliser les transitions entre les vues...................................................................... | 34 |  |
| 3.1.6 | Les boites de dialogues.......................................................................................... | 35 |  |
| 3.1.7 | Quelques astuces pour les pages made in Apple.................................................. | 35 |  |
| 3.2 | . Créer des listes............................................................................................................ | 38 |  |
| 3.2.1 | Définir une liste simple............................................................................................ | 38 |  |
|  |  |  |  |  |

**2012 ©** **Mobile****-tuts ! Actualités et tutoriels autour des technologies mobiles**2

**Développer avec jQuery Mobile – Première Édition**

3.2.2 Liste numérotée39

3.2.3 Insérer des séparateurs dans les listes39

3.2.4 Afficher un compteur dans un élément de liste40

3.2.5 Rechercher dans une liste41

3.2.6 Listes à lecture seule42

3.3 .Utiliser des boutons43

3.3.1 Définir un bouton43

3.3.2 Associer une icône à un bouton43

3.3.3 Juxtaposer les boutons horizontalement (inline)43

3.4 .Éléments de formulaires44

3.4.1 Boutons radio44

3.4.2 Sliders45

3.4.3 Élément de recherche45

3.4.4 Mieux disposer les éléments à l&#039;écran45

3.5 .Les barres d&#039;outils46

3.5.1 Barres d&#039;outils &quot;header&quot; et &quot;footer&quot;46

3.5.2 Barres d&#039;outils de type fixe47

3.5.3 Utiliser les barres de navigation47

3.6 .Travaux pratiques48

4 .Programmer avec l’API jQuery Mobile51

4.1 .Initialisation du Framework51

4.1.1 L&#039;événement mobileinit51

4.1.2 Options de configuration52

4.1.3 Événements jQuery Mobile53

4.1.4 Fonctions utilitaires55

4.2 .Manipuler des pages57

4.2.1 Gérer les attributs d&#039;une page57

4.2.2 Pré-chargement et gestion du cache57

4.2.3 Gérer ses pages de façon programmatique58

4.3 .Manipuler des listes59

4.3.1 Gérer les attributs d&#039;une page59

4.3.2 Créer une liste dynamiquement60

4.3.3 Supprimer un élément dans une liste61

4.3.4 Gérer les événements sur les listes62

4.4 .Manipuler des boutons63

4.4.1 Gérer les attributs d&#039;un bouton63

4.4.2 Agir dynamiquement sur un bouton63

4.4.3 Gérer les événements sur les boutons64

4.5 .Manipuler des champs de saisie64

**2012 ©** **Mobile****-tuts ! Actualités et tutoriels autour des technologies mobiles**3

**Développer avec jQuery Mobile – Première Édition**

| 4.5.1 | Affecter et récupérer la valeur inscrite dans un champ de saisie............................ | 64 |
| --- | --- | --- |
| 4.5.2 | Gérer les événements sur les champs de saisie..................................................... | 64 |
| 4.6 | .Manipuler des cases à cocher....................................................................................... | 65 |
| 4.6.1 | Gérer les événements sur les cases à cocher**.**...................................................... | 65 |
| 4.6.2 | Fonction de gestion des cases à cocher................................................................. | 65 |
| 4.7 | .Manipuler des boutons radio......................................................................................... | 66 |
| 4.7.1 | Gérer les événements sur les boutons radio.......................................................... | 66 |
| 4.7.2 | Fonction de gestion des boutons radio................................................................... | 66 |
| 4.8 | .Manipuler des sliders..................................................................................................... | 67 |
| 4.8.1 | Créer dynamiquement un slider.............................................................................. | 67 |
| 4.9 | .Travaux pratiques.......................................................................................................... | 67 |
| 5 .jQuery Mobile et HTML 5...................................................................................................... | 71 |
| 5.1 | .Customisation des styles et formatage de contenus...................................................... | 71 |
| 5.1.1 | Créer son propre thème......................................................................................... | 71 |
| 5.1.2 | Créer une icône personnalisée............................................................................... | 73 |
| 5.1.3 | Regrouper des éléments par colonnes.................................................................. | 74 |
| 5.1.4 | Contenus coulissants et accordéons....................................................................... | 74 |
| 5.2 | .Balises HTML 5 spéciales............................................................................................. | 76 |
| 5.2.1 | Insérer du contenu multimédia : les balises audio et video..................................... | 76 |
| 5.2.2 | Interagir avec son téléphone: les attributs email et tel............................................ | 76 |
| 5.2.3 | Autres attribut HTML 5 : search, url....................................................................... | 77 |
| 5.3 | .Persistance de données................................................................................................ | 78 |
| 5.3.1 | Stockage dans la session....................................................................................... | 78 |
| 5.3.2 | Stockage permanent côté client............................................................................. | 78 |
| 5.4 | .Utilisation de la Géolocalisation..................................................................................... | 80 |
| 5.4.1 | Connaître ses coordonnées géographiques........................................................... | 80 |
| 5.4.2 | Afficher une fenêtre Google Maps............ .............................................................. | 83 |
| 6 .Développer avec le Framework PhoneGap........................................................................... | 83 |
| 6.1 | .jQuery Mobile et PhoneGap.......................................................................................... | 83 |
| 6.2 | .Développer avec PhoneGap......................................................................................... | 83 |
| 6.2.1 | Pré-requis............................................................................................................... | 83 |
| 6.2.2 | Installation de PhoneGap........................................................................................ | 84 |
| 6.2.3 | Importer son projet jQuery Mobile .......................................................................... | 84 |
| Annexes :................................................................................................................................... | 85 |
| Émulateurs mobiles ........................................................................................................ | 85 |
| Sites et blogs.................................................................................................................... | 85 |
| Références............................................................................................................................... | 86 |

**2012 ©** **Mobile****-tuts ! Actualités et tutoriels autour des technologies mobiles**4

**Développer avec jQuery Mobile – Première Édition**

1 . Introduction au Framework

1.1 . jQuery au cœur de l&#039;internet Mobile

Pour le dire de façon sommaire, jQuery Mobile est une outil logiciel qui fonctionne de manière transparente sur toutes les plate-formes mobiles du moment. Aussi riche que sa parente jQuery, dont la renommée n&#039;est plus à faire auprès des développeurs web, jQuery Mobile est la bibliothèque JavaScript la plus adaptée pour créer des sites web à destination des smartphones et tablettes tactiles.

Avec ses presque 1,2 Milliards d&#039;utilisateurs, soit environ 17 % de la population mondiale, l&#039;internet mobile continu de croître de façon considérable. On estime, grâce à un sondage de Médiamétrie, qu&#039;en 2012 la moitié de la population française y sera connectée. La grande diversités des écrans de terminaux mobiles est devenue un véritable casse-tête pour les développeurs de sites web mobiles, soucieux de ne pas rater le passage à l&#039;ère du tout mobile.

Grâce à jQuery Mobile, il est désormais facile de créer des sites et applications web performantes, qui s&#039;adaptent à tous les types d&#039;interfaces. Aujourd&#039;hui en version 1.0, jQuery Mobile est déjà déclarée **_&quot;Innovation de l&#039;année&quot;_** par les .Net Awards ! Qu&#039;il s&#039;agisse des fenêtres et composants graphiques d&#039;interface HTML/CSS ou de l&#039;interaction du site avec des données extérieures [base de données sur un serveur distant, géolocalisation avec Google Maps...) grâce à JavaScript, jQuery Mobile (jQM) donne tous les éléments pour construire, avec une agréable facilité, des sites qui fonctionneront sur la plupart des supports mobiles actuels.

L’explosion des ventes de smartphones et le besoin toujours plus grand des internautes d’être connecté au monde a favoriser la croissance de ce type de plates-formes de développement mobile. Pour de nombreux développeurs, jQuery Mobile est tout simplement en tête du classement. L&#039;inclure dans ses projets est un donc choix absolument stratégique.

**2012 ©** **Mobile****-tuts ! Actualités et tutoriels autour des technologies mobiles**5

**Développer avec jQuery Mobile – Première Édition**

1.2 . Découvrir Le Framework

1.2.1 Installation de jQuery Mobile

Installer la plate-forme jQuery Mobile se fait aussi simplement que l&#039;installation de jQuery. Il suffit en effet de soit :

*   **Télécharger** le fichier JavaScript et de l&#039;appeler dans son fichier html. Il fautdans ce cas télécharger également:

*   *   La feuille de style **jquerymobile.css**

*   *   Le dossier d&#039;images à mettre dans le même répertoire que les fichiers.

*   **Faire un lien** vers les fichiers JavaScript et CSS directement hébergés par lesfondateurs du Framework. Cette méthode a l&#039;avantage de nous éviter de télécharger des documents (JavaScript, images).

Étant donné que jQuery Mobile dépend du Framework jQuery, celui-ci doit être invoqué bien avant l&#039;importation de jQM. Concrètement on aura avoir ceci :

Ma première Page

name=&quot;viewport&quot;content=&quot;width=device-width, initial-scale=1&quot;&gt; rel=&quot;stylesheet&quot;href=&quot;http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.css&quot; /&gt;

**Illegal HTML tag removed :** src=&quot;http://code.jquery.com/jquery-1.7.1.min.js&quot;&gt;

**Illegal HTML tag removed :** src=&quot;http://code.jquery.com/mobile/1.1.0-rc.1/jquery.mobile-1.1.0-rc.1.min.js&quot;&gt;

….

**2012 ©** **Mobile****-tuts ! Actualités et tutoriels autour des technologies mobiles**6

**Développer avec jQuery Mobile – Première Édition**

1.2.2 Une première application

Un template jQuery Mobile se définit très facilement. Il est presque toujours composé d&#039;une ou plusieurs page, définies dans un document écrit en HTML 5 :

*   Une page contenant généralement :

*   *   Un titre (entête, **header**)

*   *   Du contenu (**content**)

*   *   pied de page (**footer**)

Définition d&#039;une page de base en jQuery Mobile :

data-role=&quot;page&quot;&gt;

data-role=&quot;header&quot;&gt;