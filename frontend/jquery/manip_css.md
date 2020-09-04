#Gérer le CSS avec jQuery#

JQuery nous permet de modifier le code CSS des éléments HTML présents sur notre page. Cela permet notamment de **changer dynamiquement le style d'un site** selon les actions de l'utilisateur. Tout est rendu possible grâce à la méthode ```.css()``` qui a plusieurs utilisations que nous allons voir ensemble.

##1\.Récupérer une valeur##

Dans son usage le plus basique cette méthode nous permet de **récupérer la valeur d'une propriété css sur l'élément HTML sélectionné** en passant cette propriété en argument.

Dans l'exemple suivant mon instruction jQuery retourne la valeur de ma couleur de texte pour la classe "exemple", en l'occurrence rouge, au format RGB soit 255,0,0.

```
.exemple {
  color: red;
}

```
```
$(".exemple").css("color");

```

##2\.Changer une valeur##

Heureusement on peut faire bien plus que simplement récupérer des valeurs, on peut également les modifier. Pour cela il suffit de passer la valeur comme deuxième argument de la méthode ```.css()```.

**Vous pouvez passer toutes les valeurs et les propriétés qui existent en CSS**. Si l'élément ciblé ne possédait pas la propriété, celle-ci sera ajoutée.

Dans l'exemple suivant je change la couleur de police de ma classe exemple en bleu.

```
.exemple {
  color: red;
}

```
```
$(".exemple").css("color", "blue");

```

##3\.Changer plusieurs valeurs##

Qui a dit qu'on ne voulait modifier que la couleur de notre texte ? On a peut-être envie de modifier plusieurs propriétés et c'est là que les choses se compliquent un peu.

Pour modifier plusieurs propriétés avec notre méthode ```.css()``` nous allons devoir passer **un objet javascript en argument** qui contiendra toutes nos propriétés et leurs nouvelles valeurs.

Si vous ne savez pas ce qu'est un objet en javascript, je vous invite à consulter le premier atelier du programme de javascript avancé.

Dans l'exemple suivant nous modifions à la fois la couleur de fond, la largeur et l'ombrage de nos items avec la classe exemple :

```
$(".exemple").css({
  "background-color": "green",
  "width": "800px",
  "box-shadow": "3px 3px 3px black"
});

```

##4\.Sources##

- http://www.w3schools.com/jquery/jquery_css.asp

- https://openclassrooms.com/courses/un-site-web-dynamique-avec-jquery/manipuler-le-code-css-avec-jquery
