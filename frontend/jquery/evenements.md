#Les événements jQuery#

JQuery est **orienté sur les événements**. Les événements qui peuvent se réaliser sur une page ont été prédéfinis et nous avons la possibilité de déclencher des actions quand l'un d'eux se produit. Un événement peut être le survol d'une balise HTML par la souris ou un clic de l'internaute. **Il est toujours associé à un élément de notre page**.

Schématiquement, la syntaxe pour demander à jQuery de réaliser une action quand un événement est détecté est la suivante :

```
$("selecteur").événement(function(){
  réalise une action
});

```
Souvenez-vous de ce bout de code qui entoure nos instructions jQuery

```
$( document ).ready(function() {
});

```
Il s'agit en fait d'un événement lié au document (notre page HTML). Le chargement du contenu ```.ready()``` est un événement en jQuery.

Nous allons étudier ensemble certains des événements les plus courants. Dans leur utilisation classique, **les événement appelent une function ```function(){ }``` en argument** est c'est dans cette fonction que l'on écrit le code à éxecuter (cela peut même être une autre fonction).

 Pour découvrir tous les événements disponibles, consultez la documentation : https://api.jquery.com/category/events/

##1\. Au clic##

Chaque clic de l'utilisateur avec le bouton gauche de sa souris sur la page est un événement. Deux méthodes nous permette de déclencher une action sur cet événement

- **.click()** : déclenche une action quand l'utilisateur fait un clic gauche. Par exemple si je souhaite afficher du contenu quand l'utilisateur clic sur un titre ```<h1>``` :

```
$("h1").click(function() {
  affiche mon contenu
});

```

- **.dblclick()** : fonctionne exactement comme .click() mais se déclenche lors d'un double clic gauche de l'utilisateur.

##2\.Au survol de la souris##

A chaque fois que l'utilisateur survole un élément de notre page avec le curseur de sa souris c'est un événement. On distingue deux famille de méthodes pour déclencher des actions en conséquence :

- **.mouseenter()/.mouseleave()** : ```.mouseenter()``` permet de déclencher une action quand le curseur de la souris vient survoler un élément en particulier. ```.mouseleave()``` permet de déclencher une action quand le curseur de la souris quitte l'élément en question.

Si je veux afficher du contenu quand l'utilisateur survole un ```<h1>``` :

```
$("h1").mouseenter(function() {
  affiche mon contenu
});

```

- **.mouseover()/.mouseout()** : elles sont très proches des deux méthodes vues précédemment et s'utilise de la même manière. La seule différence est qu'elles s'appliquent également aux balises enfants de celle sélectionnée.

Par exemple, dans le cas suivant le contenu sera affiché quand l'utilisateur survolera la ```<div>``` de classe "main" mais également la ```<div>``` de classe "second":

```
<div class="main">
 <div class="second">
 </div>
</div>

```

```
$(".main").mouseover(function() {
  affiche du contenu
});

```

##3\.Boutons de la souris##

Lorsque l'utilisateur appuie ou relâche les boutons de sa souris c'est un événement. JQuery met deux méthodes à notre disposition pour déclencher des actions en conséquence :

- **mousedown** : déclenche une action quand l'utilisateur reste appuyé sur n'importe quel buton de sa souris.

- **mouseup** : déclenche une action quand l'utilisateur relâche que le bouton de sa souris

Par exemple, si je veux afficher du contenu quand l'utilisateur reste appuyé sur un ```<h1>``` :

```
$("h1").mousedown(function() {
  affiche mon contenu
});

```

##4\.Formulaires##

La gestion des formulaires côté front est très importante pour l'expérience utilisateur. Heureusement plusieurs événements nous permettent de déclencher des actions quand l'utilisateur interagi avec nos formulaires. Nous en présenterons 2 :

- **.focus()** : permet de déclencher une action quand l'utilisateur sélectionne un champ du formulaire pour le remplir

- **.blur()** : permet de déclencher une action quand l'utilisateur quitte le champ du formulaire

Par exemple je peux changer la couleur de fond des inputs de mon formulaire quand l'utilisateur est entrain d'écrire dedans :

```
$("input").focus(function(){
  change la couleur de fond
});

```

##5\.Sources##

- http://www.w3schools.com/jquery/jquery_events.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/les-bases-de-la-gestion-evenementielle
