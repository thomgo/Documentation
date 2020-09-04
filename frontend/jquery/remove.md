# Supprimer des éléments

Il est possible de supprimer des éléments HTML avec jQuery. Cela peut-être utile pour gérer le parcours utilisateur sur son site. C'est-à-dire **supprimer des éléments selon les choix réalisés par l'internaute**.

Par exemple dans un formulaire certains champs peuvent disparaître quand un utilisateur répond à une question à choix multiples.

## 1\. Tout supprimer avec .remove()

La méthode ```.remove()``` vous permet de supprimer un élément sur votre page, sachez cependant qu'**elle supprimera aussi ses éléments enfants**.

Dans l'exemple suivant je supprime la ```<div>``` de classe test mais je supprime aussi le ```<p>``` qu'elle contient :

```

<div class="test">
  <p>Voilà du contenu texte</p>
</div>

```

```
  $(".test").remove();

```

## 2\. Vider un élément avec .empty()

Cette méthode fonctionne sur le même principe que la précédente à la différence qu'elle ne **supprime que les enfants de l'élément sélectionné**.

Dans l'exemple précédent, j'aurais donc supprimé le ```<p>``` mais conservé la ```<div>``` avec l'instruction suivante :

```
  $(".test").empty();

```

## 3\. Sources

- http://www.w3schools.com/jquery/jquery_dom_remove.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/inserer-et-remplacer-des-elements-dans-le-dom
