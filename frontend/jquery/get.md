# Récupérer du contenu avec jQuery

JQuery nous propose un ensemble de méthodes appelés getters. En anglais to get signifie "obtenir", les getters sont donc **des méthodes qui permettent de récupérer du contenu** sur la page. Il peut s'agir de contenu texte, html et bien d'autres qui peut par la suite être stocké dans une variable et réutilisé.

Nous allons voir ensemble les principaux getters.

La syntaxe sera la suivante :

```
$("élement").getter();

```

## 1\.Contenu texte

Pour récupérer le contenu texte d'une balise HTML, nous pouvons utiliser le getter ```.text()``` de jQuery. Ainsi si je veux récupérer le contenu texte d'un élément avec l'id "content" je peux écrire :

```
<p id="content">Contenu texte</p>

```

```
var texte = $("#content").text();

```
Notre variable texte contiendra une string "Contenu texte". Vous êtes ensuite libre de réutiliser le contenu de cette variable comme bon vous semble.

## 2\.Contenu texte et HTML

Avec le getter précédent, on ne peux récupérer que du contenu texte, si l'on souhaite récupérer également d'éventuelles balises inline il faut utiliser le getter ```.html()``` dans ce cas.

Par exemple :

```
<p id="content"><span>Contenu texte</span></p>

```

```
var texte = $("#content").html();

```
Notre variable texte contiendra la string "<span>Contenu texte</span>"

## 3\.Contenu des formulaires

Que faire cependant si vous voulez récupérer le contenu d'un champ de formulaire pour avertir l'utilisateur d'une éventuelle erreur ? Les getters ```.text()``` et ```.html()``` ne fonctionneront pas, il faut utiliser un getter particulier ```.val()```.

Si je veux récupérer le contenu d'un input portant l'id "content", je peux écrire :

```
var texte = $("#content").val();

```

## 4\.Contenu des attributs

Lors de vos développements front, il y a probablement un dernier type de contenu que vous souhaiterez récupérer, il s'agit de la valeur des attributs dans les balises HTML.

Là encore jQuery dispose d'un getter spécial ```.attr()```. Son usage est légèrement différent car il faut spécifier en argument le type d'attribut ciblé.

Si je veux récupérer l'attribut ```href``` d'un lien sur ma page je peux écrire :

```
<a href="www.google.com">Mon lien</a>

```

```
$texte = $("a").attr("href");

```
Notre variable texte contiendra la string "www.google.com"

## 5\.Sources

- http://www.w3schools.com/jquery/jquery_dom_get.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/modifier-le-contenu-d-un-element
