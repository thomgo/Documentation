# Ajouter du contenu

Jusqu'à maintenant nous avons travaillé sur le contenu déjà existant mais que diriez vous de pouvoir ajouter votre contenu directement sur vos pages avec jQuery ?

Pour cela nous avons plusieurs fonctions à notre disposition, il faut seulement faire la **distinction entre celles qui ajoutent du contenu à l'intérieur de l'élément sélectionné et celle qui l'ajoute à l'extérieur**.

Regardons cela ensemble.

## 1\.Ajouter du contenu à l'intérieur des balises

- **append** : elle permet d'ajouter du contenu à la fin de l'élément.

Dans l'exemple suivant j'ajoute un ```<span>``` juste avant la fermeture de la balise ```<p>```

```
<article>
  <p>Un paragraphe de texte</p>
</article>

```

```
$("p").append("<span>Du texte rajouté</span>");

```

Le résultat sera :

```
<article>
  <p>Un paragraphe de texte<span>Du texte rajouté</span></p>
</article>

```

- **prepend** : cette méthode fonctionnement exactement sur le même principe que la précédente si ce n'est que le contenu est ajouté au début de l'élément sélectionné.

Dans l'exemple précédent :

```
$("p").prepend("<span>Du texte rajouté</span>");

```
Affichera en fait

```
<article>
  <p><span>Du texte rajouté</span>Un paragraphe de texte</p>
</article>

```

## 2\.Ajouter du contenu à l'extérieur des balises

- **after** : elle permet d'ajouter du contenu juste après l'élément sélectionné.

Dans l'exemple suivant, j'ajoute un ```<p>``` juste après le premier

```
<p>Mon premier paragraphe</p>

```

```
$("p").after("<p>Mon deuxième paragraphe</p>");

```
Le résultat affiché sera :

```
<p>Mon premier paragrahe</p>
<p>Mon deuxième paragraphe</p>

```

- **before** : elle fonctionne sur le même principe que la fonction précédente mais permet d'ajouter le contenu avant l'élément.

Si nous reprenons notre exemple avec :

```
$("p").before("<p>Mon deuxième paragraphe</p>");

```

Le résultat affiché sera :

```
<p>Mon deuxième paragrahe</p>
<p>Mon premier paragraphe</p>

```
## 3\.Ajouts mutliples

Pour l'ensemble des méthodes évoquées précédemment, il est possible de **rajouter plusieurs éléments à la fois**, il suffit pour cela de les passer en paramètres de la fonction.

Si par exemple je souhaite ajouter plusieurs ```<span>``` à l'intérieur d'un paragraphe je peux écrire :

```
$("p").append("<span>texte 1</span>", "<span>texte 2</span>", "<span>texte 3</span>");

```

## 4\.Sources

- http://www.w3schools.com/jquery/jquery_dom_add.asp

- https://openclassrooms.com/courses/simplifiez-vos-developpements-javascript-avec-jquery/inserer-et-remplacer-des-elements-dans-le-dom
