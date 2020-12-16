# Utiliser les composants Bootstrap

Parmi toutes les possibilités offertes par Bootstrap, il y a un outil qui vous fera gagner beaucoup de temps et dont il serait dommage de se priver, se sont **les composants**

## 1\. Qu'est ce qu'un composant ?

Nous en avions déjà parlé brièvement mais il peut être utile de revenir dessus. Un composant est un bloc de code plus ou moins prêt à l'emploi qui correspond à un élément de base sur un site.

Autrement-dit, les développeurs de Bootstrap on isolés les éléments qui revenaient le plus souvent sur les sites internet et en proposent des **versions à disposition sur le site de la documentation Bootstrap**.

Il faut donc voir les composants un peu comme les **différents produits d'un supermarché du web**. Au lieu d'aller à la ferme faire pousser des légumes, vous n'avez qu'à aller les chercher en rayon !

Lorsque vous irez chercher le code des composants sur le site officiel, vous récupérerez la plupart du temps uniquement un code HTML agrémenté de **multiples classes**. Celles-ci renvoient au CSS Bootstrap et permettent de mettre votre HTML en forme. Dans certains cas vous verrez également des attributs qui permettent de déclencher des événements gérés par JavaScript.

Parmi les composants, on trouve entre autres :

- des cartes
- des headers/footers
- des formulaires
- des bouttons
- des paginations
- et plein d'autres choses incroyables

Pour obtenir la liste complète de tous les composants Bootstrap, rendez-vous à cette adresse : https://v4-alpha.getbootstrap.com/components/alerts/

Dans la partie suivante, nous allons vous présenter quelques composants pour l'exemple mais cela ne vous évitera pas d'aller **consulter la documentation**. Celle-ci est complète, claire et exhaustive, ce tutoriel n'est qu'une entrée en matière.

## 2\. Présentation de quelques composants

### A\.Jumbotron

Le jumbotron (https://v4-alpha.getbootstrap.com/components/jumbotron/) est un des éléments les plus **basiques** de Bootstrap mais aussi l'un des plus **simples** et plus fréquemment **utilisés**.

Il s'agit en fait tout simplement d'un **conteneur** qui permet de mettre en avant, sur toute la largeur de l'élément parent, **un message au contenu clef et percutant**. Bien souvent il est utilisé pour faire des headers, des bannières commerciales, voire des footers.

Dans sa forme la plus simple dans la documentation voilà le code d'un jumbotron :

```
<div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1 class="display-3">Fluid jumbotron</h1>
    <p class="lead">This is a modified jumbotron that occupies the entire horizontal space of its parent.</p>
  </div>
</div>

```
Remarquez le nombre de classe qui permettent de mettre en forme notre contenu. Vous devez vous souvenir de la classe ```container```, c'est elle qui permet d'avoir une marge entre le texte et le bord du conteneur parent.

NB: n'oubliez pas de mettre des balises sémantiques quand vous le pouvez pour éviter de multiplier les divs. Ici vous pouvez facilement les transformer en ```<header>``` et ```<section>```

Bon pour l'instant, je vous l'accorde ce jumbotron est un peu triste tout en noir et gris mais nous verrons dans le chapitre suivant qu'avec quelques classes supplémentaires nous pouvons lui donner un super look !

### B\.Nav

Avez-vous déjà vu un site sans un menu ? Nous en tout cas jamais et les développeurs de Bootstrap l'ont bien compris, c'est pourquoi ils proposent tout un **ensemble de composants appelés navs et navbars qui permettent de mettre rapidement en place des menus sur votre site**.

https://v4-alpha.getbootstrap.com/components/navbar/

Pour notre exemple, nous travaillerons avec une navbar mais sachez qu'il n'y a pas de grande différence avec une simple nav.

Disons que normalement, la navbar est utilisée pour faire la **navigation principale du site**, celle qui ne change jamais, alors que la nav est utilisée pour faire des **petites navigations internes** qui peuvent changer selon les pages (pour des ancres par exemple).

Si nous allons chercher une navbar dans son état le plus simple, c'est-à-dire sans menu déroulant et sans bar de recherche, voilà ce que l'on récupère comme code :

```
<nav class="navbar navbar-toggleable-md navbar-light bg-faded">
          <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <a class="navbar-brand" href="#">Link</a>

          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
              <li class="nav-item active">
                <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Link</a>
              </li>
              <li class="nav-item">
                <a class="nav-link disabled" href="#">Disabled</a>
              </li>
            </ul>
          </div>
        </nav>

```
Le code à l'air imposant au premier abord mais en réalité il n'est pas très compliqué et permet de faire un **menu positionné proprement** et surtout **responsive**, puisque sur smartphone il sera remplacé par un icône cliquable.

Si l'on regarde le HTML, on retrouve bien une ```<nav>``` qui contient une ```<ul>``` soit la composition classique d'un menu.

Les classes sont un peu plus compliquées à comprendre mais on peut en repérer trois principales :

- ```navbar``` : la classe de base pour réaliser une navbar avec son style

- ```navbar-toggleable```: indique que la nav sera remplacée par un icône sur smartphone

- ```navbar-collapse```: détermine le contenu qui sera masqué sur smartphone

- ```nav-item```: stylise un élément de menu

- ```nav-link```: stylise un lien de menu

Une fois cela compris vous pouvez rajouter le nombre d'éléments qui vous fait plaisir dans votre menu et/ou changer le contenu des liens.

De base celui-ci est dans les tons gris mais vous verrez dans la documentation que vous pouvez facilement le styliser.

### C\.Card

Les cartes sont également un des éléments les plus utilisés de Bootstrap, elle permette de **définir de mettre en avant du contenu sous forme de bloc** de manière simple et intuitive.

Elles sont souvent utilisées pour réaliser des **articles de news** sur les blogs ou encore des **fiches produits** sur les sites e-commerce. Concrètement, les cartes correspondent aux articles que vous avez mis dans plusieurs de vos projets jusqu'ici.

Bootstrap propose une large variété de cartes aux styles et à la mise en formes différents (https://v4-alpha.getbootstrap.com/components/card/). Elles ont pour intérêt de très bien se positionner avec la grille (les développeurs de Bootstrap ont pensé à tout ;-)).

Voilà un exemple de carte simple, il contient une image d'en tête, un titre, un petit texte de description et un lien qui fait office de button :

```
<div class="card" style="width: 20rem;">
  <img class="card-img-top" src="..." alt="Card image cap">
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>

```

Il existe plein d'autres modèles de cartes, à vous de choisir celui qui vous convient le mieux et si besoin de le personnaliser vous-même ensuite.

Rendez-vous également de remplacer les div par des balises sémantiques !

### D\.Carousel

Dernier composant de notre présentation, le carrousel ou slider. **Il permet de mettre facilement du contenu de type image et texte en avant en changeant dynamiquement l'image d'en tête du site et son texte**.

Vous en avez probablement déjà vus sur des sites. Il s'agit d'un élément très courant car l'effet visuel est immédiat et le contenu dans le slider reçoit souvent plus de cliques.

Souvent les sliders sont un mélange de CSS et de JavaScript et mis à part quelques variations dans le code, celui est plus ou moins similaire sur tous les sliders.

Il ne faut donc pas passez votre temps à réinventer la roue, Bootstrap vous propose plusieurs types de sliders élégants et fonctionnels à disposition (https://v4-alpha.getbootstrap.com/components/carousel/).

Voici le modèle le plus simple qui permet simplement de faire défiler des images avec un petit bandeau de texte sur la base de l'attribut ```alt``` :

```
  <div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
          <div class="carousel-inner" role="listbox">
            <div class="carousel-item active">
              <img class="d-block img-fluid" src="..." alt="First slide">
            </div>
            <div class="carousel-item">
              <img class="d-block img-fluid" src="..." alt="Second slide">
            </div>
            <div class="carousel-item">
              <img class="d-block img-fluid" src="..." alt="Third slide">
            </div>
          </div>
        </div>

```
Une fois ce code intégré à votre site, il ne vous reste plus qu'à modifier l'attribut ```src``` des images pour que cela corresponde à un chemin valide dans votre dossier et écrire la description dans l'attribut ```alt```

## 3\. Exercices

## 4\. Sources

- https://v4-alpha.getbootstrap.com/components/carousel/
