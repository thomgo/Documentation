#Gérer les classes en jQuery#

Après avoir suivi le parcours HTML et CSS, vous utilisez probablement les classes dans vos pages web pour appliquer le même style à plusieurs balises HTML. JQuery vous permet de modifier dynamiquement l'attribut ```class``` de vos éléments HTML.

##1\. Ajouter une classe##

Vous pouvez ajouter une classe à votre élément grâce à la méthode ```.addClass()```. **L'élément prendra alors les propriétés associées à la classe**.

Dans l'exemple suivant j'ajoute la classe danger à mon paragraphe ce qui a pour effet de passer le fond en rouge et le texte en blanc.

```
<p class="test">Voilà du contenu texte</p>

```
```
.newclass{
  background-color: red;
  color: white;
}

```

```
$(".test").addClass("newclass");

```

##2\. Retirer une classe##

De la même manière nous pouvons très simplement retirer des classes à nos attributs HTML en utilisant une autre méthode de jQuery ```.removeClass("nom de la classe")```. Une fois cette méthode lancée, **l'élément ciblé n'aura plus la classe dans ses attributs et en perdra les propriétés**.

Dans l'exemple suivant mon paragraphe ne sera pas écrit sur fond rouge car je lui ai retiré la classe correspondante :

```
<p class="info">test</p>

```

```
.info {
  background-color: red;
}

```

```
$("p").removeClass("info");

```

##3\. Retirer et ajouter une classe en même temps##

La méthode qui suit est un peu plus compliquée à comprendre mais elle vous sera extrêmement utile lors de vos développements.

Bien souvent les éléments sur un site changent en fonction des actions des utilisateurs. **Cela vous oblige fréquemment à enlever et retirer des classes** pour modifier l'aspect de vos balises HTML dynamiquement.

**Pour vous éviter des lignes de code inutiles**, les développeurs de jQuery ont pensé à tout et ont créé la méthode ``` .toggleClass("nom de classe") ```. **Cette méthode check si l'élément sélectionné porte déjà la classe**, si c'est le cas alors elle la retire, sinon elle l'ajoute.

Dans l'exemple suivant, au premier lancement de l'instruction le paragraphe obtiendra la classe ```info``` et son fond passera en rouge, si l'instruction est relancée, il perdra la classe et son fond reprendra sa couleur d'origine.

```
<p>test</p>

```

```
.info {
  background-color: red;
}

```

```
$("p").toggleClass("info");

```

##4\. Sources##

- http://www.w3schools.com/jquery/jquery_css_classes.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/modifier-le-contenu-d-un-element
