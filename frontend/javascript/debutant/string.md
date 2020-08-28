# Les chaînes de caractères en JavaScript

Nous vous avons déjà présenté les strings au chapitre précédent, normalement vous devez vous souvenir qu'il s'agit simplement de texte. Mais comme vous vous en doutez il y a un peu plus de choses à dire à leur sujet.

## 1\.Les chaînes de caractères: bases

Comme nous l'avions dit précédemment on repère une chaîne de caractères parce qu'elle est **entourée de guillemets** mais quel type de guillemets ? Simples ou doubles ? En JavaScript les **deux types sont acceptés**, ainsi les deux exemples suivants seront considérés comme du texte :

```
"Voici une chaîne de caractère"

'Voici une chaîne de caractère'

```
**Attention** par contre à ne jamais oublier les guillemets, autrement l'ordinateur ne saura pas qu'il a affaire à du texte et traitera vos informations différemment.

## 2\. Allons plus loin avec les strings

Que se passera-t-il si il y a une apostrophe dans notre string ? Une apostrophe n'est rien de plus qu'une guillemet simple, il y a donc un risque de confusion pour l'ordinateur qui ne saura plus où commence et où s'arrête notre chaîne de caractères.

Dans ce cas on dit qu'il faut échapper le caractère, c'est à dire expliquer à l'ordinateur que cette guillemet fait partie de notre texte.

Pour ce faire on utilise un ```\``` avant le caractère à échapper. Ainsi la string suivante est correcte :

```
'La voiture de l\'autre'

```

Mais celle-ci provoquera une erreur

```
'La voiture de l'autre'

```

Sachez qu'en JavaScript il existe bien d'autres caractères dits spéciaux à échapper mais vous les verrez plus tard. Sachez également qu'en ce qui concerne les guillemets, si vous utilisez des guillemets doubles vous n'avez pas besoin de l'échappement. La string suivante est donc correcte :

```
"La voiture de l'autre"

```

## 3\.Que faire avec nos chaînes de caractères ?

Pour l'instant, nous pouvons nous demander l'utilité des chaînes de caractères, en effet à ce stade leur usage semble limité. Vous verrez pourtant plus tard qu'on peut faire des choses incroyables grâce à elles :

- Dialoguer avec l'internaute

- Recevoir des information de l'internaute

- Les mesurer

- Les réorganiser

- Extraire des informations particulières

## 4\. Sources

- http://www.w3schools.com/jsref/jsref_obj_string.asp

- http://www.w3schools.com/js/js_datatypes.asp
