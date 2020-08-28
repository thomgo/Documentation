# Les types primitifs en JavaScript

Vous devez probablement vous demandez de quoi il s'agit ! En fait ce sont encore des termes compliqués pour exprimer des notions simples.

En JavaScript et comme avec tout langage de programmation, nous travaillons avec **des données** qui sont traitées par l'ordinateur. Si nous reprenions notre programme ```faire du thé```, le thé ou l'eau seraient des données par exemple.

Ces données peuvent être de différents genres (type) pour être reconnues par l'ordinateur. En JavaScript on compte 5 genres de base (primitifs). Il faut voir ces types primitifs comme des matériaux élémentaires avec lesquels l'ordinateur peut travailler.

Toujours dans notre programme ```faire du thé``` vous pouvez travailler avec l'eau ou le thé mais vous ne pouvez pas travailler avec de l'essence et bien c'est pareil en JavaScript on ne peut travailler qu'avec certains types de données.

## 1\.String

Les strings sont le premier type de données avec lequel nous pouvons travailler, il s'agit en fait de chaînes de caractères ou plus simplement... de **texte**. En même temps il semble assez logique que l'ordinateur puisse travailler avec du texte non ?

On reconnaît une string parce qu'elle est **entourée de guillemets**, ainsi la phrase suivante dans un programme JavaScript sera considérée de type string (texte) :

```
"Voici une phrase d'exemple de type string"

```

## 2\.Number

Les nombres font également partie des types de données basiques utilisés en JavaScript, là encore rien de surprenant après tout les ordinateurs sont bien là pour faire des calculs à notre place !

On reconnaît un nombre parce qu'il est écrit au **format numérique** et jamais sous forme de texte. Ainsi les exemples suivant seront considérés comme des nombres :

```
4

5.36

-45

```

## 3\.Boolean

Voilà un type de données basique et puissant mais qui peut être difficile à comprendre. Cependant il vaut mieux apprendre à s'en servir car on le rencontre fréquemment en programmation.

**Un boolean ne peut prendre que 2 valeurs ```true``` ou ```false```. **

Autrement-dit l'ordinateur peut recevoir des informations qui sont vraies (true) ou fausses (false)

Nous verrons plus en détails ce que cela implique dans le chapitre réservé au boolean, ne vous inquiétez donc pas si cela n'est pas clair.

## 4\.Null

Voilà un autre type de données quelque peu abstrait. Une valeur ou une donnée de type null est nulle. Pas très utile me direz-vous ?

En fait cela veut dire que notre valeur existe mais qu'elle ne contient rien, sa valeur est nulle.

## 5\.Undefined

On pourrait, à tort croire que ```undefined``` est équivalent à null, en réalité il y a une grande différence.

En fait une donnée ou valeur ```undefined``` n'a pas été déclarée, autrement-dit pour l'ordinateur elle n'existe pas et il ne peut pas savoir ce qu'elle contient. Vous devez éviter de vous retrouver avec des valeurs ```undefined```.

## 6\.En résumé

En JavaScript, il y a 5 types de base pour nos données :

- texte

- nombres

- boolean (vrai ou faux)

- null (valeur égale à 0)

- undefined (valeur qui n'existe pas)

## 7\.Sources

- https://developer.mozilla.org/fr/docs/Glossaire/Primitive

- https://developer.mozilla.org/fr/docs/Web/JavaScript/Structures_de_donn%C3%A9es

- http://www.w3schools.com/js/js_datatypes.asp
