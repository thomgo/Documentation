# Comment utiliser Bootstrap ?

Voilà, Bootstrap est enfin installé dans votre projet et vous êtes prêt à travailler avec lui. Mais au fait, comment ça marche Bootstrap ? Avant de rentrer dans les entrailles de ce framework, prenons quelques minutes pour comprendre ses grands principes de fonctionnement. Vous allez voir pourquoi nous gagnons beaucoup de temps à utiliser un framework.

Avant toute chose sachez qu'en travaillant avec Bootstrap il faudra vous référer à la **documentation** en permanence et c'est ce que nous ferons à partir de maintenant. Vous trouverez la documentation à cette adresse : https://v4-alpha.getbootstrap.com/getting-started/introduction/ . Remarquez la quantité de catégories sur la droite, ça en fait des choses à voir !  

## 1\.Des morceaux de codes prêts à l'emploi

Vous l'avez sans doute remarqué, la plupart des sites, voire tous les sites commencent avec un header, puis on trouve une navigation etc... Ces éléments seront présents quoiqu'il arrive et la plupart du temps, le code HTML et styles de base sont très similaires sur tous les sites.

Bootstrap l'a bien compris et vous permet de gagner du temps en vous proposant des **"morceaux" de pages prêts à l'emploi** que vous n'avez plus qu'à personnaliser par la suite. Vous pouvez par exemple récupérer dans la documentation un header que vous n'avez plus qu'à intégrer à votre site.

Pour cela dans la documentation, rendez-vous dans la partie "Components", puis "Jumbotron". Comme vous le voyez vous avez deux types de header à disposition. Vous n'avez plus qu'à choisir celui qui vous convient et mettre son code en début de page, par exemple :

```

<div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1 class="display-3">Fluid jumbotron</h1>
    <p class="lead">This is a modified jumbotron that occupies the entire horizontal space of its parent.</p>
  </div>
</div>

```
Voilà votre site a déjà plus d'allure, non ? Et vous n'avez pas eu à vous soucier du HTML et du CSS. Bon par contre les choses seraient un peu trop belles s'il suffisait de ne faire que ça. Tout au long de nos cours, nous avons insisté sur le HTML sémantique, or là comme vous le voyez, il y a **beaucoup de ```<div>``` ce qui n'est pas très bon.**

Prenez donc 30 secondes pour transformer toutes ces vilaines ```<div>``` en un beau HTML sémantique. Voilà ce que vous pourriez obtenir :

```
<header class="jumbotron jumbotron-fluid">
  <section class="container">
    <h1 class="display-3">Fluid jumbotron</h1>
    <p class="lead">This is a modified jumbotron that occupies the entire horizontal space of its parent.</p>
  </section>
</header>

```

Mais je ne vais pas perdre **la mise en forme** en faisant cela ? Non car ce sont **les classes qui s'en occupent** et nous n'y avons pas touché ! Bootstrap vous propose plein d'autres composants, nous reviendrons sur les principaux plus tard.

## 2\.Des classes prêtes à l'emploi

Nous avons déjà commencé à en parler, dans Bootstrap ce sont **les classes qui s'occupent principalement de la mise en forme**. Vous avez donc accès à tout un ensemble de classes que vous pouvez ajouter à une structure HTML déjà existante pour lui appliquer une **mise en forme propre et professionnelle.**

Prenons un exemple très simple, admettons que vous souhaitiez que votre ```<header>``` ait un fond bleu et que tout les textes soient écrits en blanc et bien si vous allez dans le rubrique "Utilities" puis "Colors" de la documentation, vous verrez qu'il suffit de lui appliquer deux classes ```bg-primary``` et  ```text-white```. Ce qui nous donne :

```
<header class="bg-primary text-white">
   <h1>Test</h1>
</header>

```

Là encore, il existe de très nombreuses classes pour la mise en forme et nous verrons les principales un peu plus loin dans notre étude de Bootstrap. Nous verrons que Bootstrap nous permet même de faire du JavaScript !

Attention toutefois à ne pas tomber dans **un piège classique, à savoir vous reposer complètement sur Bootstrap**. Il s'agit d'un très bon framework, mais ce n'est qu'un framework, il ne fera pas votre site à votre place, il est là uniquement pour poser les bases. C'est à vous ensuite de **modifier/améliorer les éléments et styles de base proposés** comme nous l'avions fait plus haut en rajoutant de la sémantique dans le HTML par exemple.

## 3\.Sources

- https://v4-alpha.getbootstrap.com/getting-started/introduction/
