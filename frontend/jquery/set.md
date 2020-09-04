#Modifier du contenu avec jQuery#

Vous savez maintenant récupérer du **contenu** sur votre page mais ce serait bien de **pouvoir aussi le modifier**. Pour ça en jQuery, il y a les setters, de l'anglais to set: "mettre". Nos setters sont en fait les mêmes méthodes que nos getters si ce n'est que l'on passe en argument notre nouveau contenu.

La syntaxe sera la suivante :

```
$("élément").setter(contenu);

```

##1\.Contenu texte##

Pour modifier le contenu texte d'une balise on utilisera donc le setter ```.text("votre nouveau texte")```.

Ici par exemple, notre paragraphe affichera "Un autre texte" au lieu de "Contenu texte".

```
<p id="content">Contenu texte</p>

```

```
$("#content").text("Un autre texte");

```

##2\.Contenu texte et HTML##

Si vous souhaitez modifier le contenu texte d'un élément tout en insérant du code HTML, vous devrez alors utiliser le setter ```.htm()```.

Dans l'exemple suivant, notre paragraphe avec l'id "content" affichera "Un nouveau texte" au lieu de "Contenu texte". "Un nouveau" sera écrit en gras. Avec un setter ```.text()``` on aurait vu les balises ```<strong>``` écrites comme du texte.

```
<p id="content">Contenu texte</p>

```

```
$("#content").html("<strong>Un nouveau</strong>texte");

```

##3\.Contenu des formulaires##

Nous l'avions vu au chapitre précédent, il est possible de récupérer le contenu d'un champ de formulaire. Avec le setter ```.val()``` il est également possible de modifier le contenu d'un champ.

Cela est particulièrement utilise pour conserver les données de l'utilisateur et lui éviter de perdre ses données au cas où un problème survient avec le formulaire.

Dans l'exemple suivant l'input du formulaire sera systématiquement pré-rempli avec "Un nouveau texte" quand l'utilisateur arrive sur la page ou la recharge.

```
<form action="">
  <input type="text">
</form>

```

```

$("input").val("Un nouveau texte");

```

##4\.Contenu des attributs

Vous pouvez également modifier le contenu des attributs de vos balises HTML avec le setter ```.attr()```.

On peut par exemple **modifier la source d'une image** et ainsi changer l'image d'un slider quand l'utilisateur clique sur une flèche.

Dans l'exemple ci-dessous, au lieu d'afficher monimage.jpg, nous afficherons nouvelleimage.jpg.

```
  <img class="slider" src="../img/monimage.jpg" alt="une image">

```

```

$(".slider").attr("href", "../img/nouvelleimage.jpg");

```

##5\.Sources##

- http://www.w3schools.com/jquery/jquery_dom_get.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/modifier-le-contenu-d-un-element
