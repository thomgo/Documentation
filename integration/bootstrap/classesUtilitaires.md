# Mise en forme avancée avec les classes utilitaires

Nous vous en avons parlé plusieurs fois dans les chapitres précédents, il existe dans Bootstrap tout un ensemble de classes que l'on peut rajouter à l'envie sur nos éléments pour améliorer leur style.

Il en existe des dizaines, nous ne vous les présenteront pas toutes ici, l'objectif est juste que vous compreniez le principe. Ensuite, il faudra vous référer à la documentation : https://v4-alpha.getbootstrap.com/utilities/borders/

## 1\.Les couleurs

Bootstrap vous offre plusieurs classes qui vous permettront d'appliquer rapidement les couleurs les usuels à votre site (https://v4-alpha.getbootstrap.com/utilities/colors/). L'avantage de ces classes est qu'elles peuvent s'appliquer autant sur le background d'un élément que sur du texte. Fini maintenant les composants tout gris !

Par contre ne rêvez pas, vous ne pourrez pas faire toute la charte graphique de votre site avec les couleurs proposées par bootstrap, il faudra quand réalisez vous-même votre charte graphique.

En fait sur un site il y a de grands thèmes qui reviennent souvent comme l'information, la validation d'une action, son refus etc... Les développeurs de Bootstrap ont donc implanté des codes couleurs relatifs à ces thèmes. Il sont parfaits pour appliquer rapidement quelques couleurs de base à une application.

Parmi les grandes thématiques de couleurs on trouve :

- primary : bleu sombre

- success: vert clair

- info: bleu clair

- warning: orange

- danger: rouge

Ces thèmes peuvent être appliqués au background d'un élément, ainsi ```bg-primary``` donnera un fond bleu sombre à l'élément qui porte cette classe, par contre ```text-success``` passera la couleur du texte dans cet élément en vert.

NB: le texte peut aussi être passé en blanc ou en gris grâce à ```text-white``` et ```text-muted```.

Ainsi si nous reprenons le jumbotron présenté dans les composants et que nous souhaitions lui appliquer un fond bleu et un texte blanc cela donnerait :

```
<div class="jumbotron jumbotron-fluid bg-primary text-white">
  <div class="container">
    <h1 class="display-3">Mon test Bootstrap</h1>
    <p class="lead">Voilà un petit site tout simple entièrement réalisé sous Bootstrap</p>
   </div>
</div>

```

## 2\.Les marges

Au cours de vos développements, vous avez dû vous en rendre compte, gérer les margins et les paddings de vos éléments prend du temps.

Grâce à Bootstrap, vous allez maintenant pouvoir le faire directement en ajoutant des classes à vos éléments.

Ces classes sont constituées de la manière suivante : (propriété)(direction)-(valeur).

- propriété : il s'agit de la margin ou du padding, respectivement représentées par un m ou un p

- direction : il s'agit de top, right, bottom, left respectivement représentés par t, r, b et l. Le couple top/bottom est représenté par un y et le couple left/right par un x.

- valeur : 6 valeurs sont disponibles de 0 à 5. 0 signifiant l'absence de margin ou de padding et 5 le plus grand espacement. Ces valeurs prédéfinies s'adaptent la plupart du temps très bien au système de grille et suffisent amplement.

Si tout cela n'est pas clair, voilà quelques exemples :

- margin-bottom à 0: ```mb-0```

- padding-left à 5: ```pl-5```

- margin left à 2 et right à 3: ```mx-2 my-3```

## 3\.Sizing et positionnement

Pour finir sur les classes utilitaires et vous montrez leur étendue, nous allons brièvement vous présenter quelques classes pour le sizing et le positionnement mais encore une fois ce sera à vous de faire l'effort d'aller rechercher ce qu'il vous faut dans la documentation.

### A\.Sizing

Vous pouvez gérer la taille de vos éléments (width et height) de vos éléments en %. Un peu comme pour les marges les classes se composent de la manière suivante: (propriété)-(valeur). Vous avez 4 valeurs à disposition : 25, 50, 75 et 100.

Exemple :

largeur de 75%: ```w-75```

hauteur de 50%: ```h-50```

### B\.Positionnement

La plupart des techniques de positionnement traditionnelles, que cela soit le display ou flexbox ont un équivalent en classes Bootstrap. L'avantage de leur utilisation est de garder un CSS clair et d'éviter de multiplier les règles.

Voilà quelques exemples pour information, à vous d'aller vous renseigner :

- gérer le display des éléments (https://v4-alpha.getbootstrap.com/utilities/display-property/): ```d-inline-block``` passera par exemple l'élément en inline-block.

- flexbox (https://v4-alpha.getbootstrap.com/utilities/flexbox/): ```d-flex``` transformera l'élément en conteneur flexbox, à vous ensuite de rajouter les class nécéssaires pour gérer la position des éléments.

## 3\.Exercices



## 4\.Sources

- https://v4-alpha.getbootstrap.com
