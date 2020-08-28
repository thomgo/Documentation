# Retour sur null et undefined

Nous sommes passés rapidement sur ces deux types lors de l'introduction aux 5 types primitifs, c'est parce qu'il aurait été compliqué de vous expliquer de quoi il retourne sans que vous sachiez ce que sont les variables.

## 1\.Quand utilise t-on ces types ?

Ces types sont utilisés pour **exprimer le vide**, autrement-dit l'absence de données. Pourquoi se soucier de l'absence de données me direz-vous ?

En fait il est fréquent quand on pense un programme de **prévoir en avance les variables dont on va avoir besoin** parce qu'on sait quelles informations nous allons récupérer. Dans ce cas une pratique courante consiste à définir des **variables vides que nous viendrons remplir par la suite**.

Ces variables peuvent avoir une valeur ```null```

```
var name = null;

```

Ou ```undefined```

```
var name;

```

Il arrive aussi parfois que l'on souhaite récupérer une valeur ou un contenu qui n'existe pas et dans ce cas notre variable reste vide.

## 2\.Différence entre null et undefined

Vous avez dû remarquer ci-dessus une différence dans la notation de nos variables, nous n'avons pas écrit ```var name = undefined;``` mais juste ```var name;```.

Cette deux notations tiennent à la différence de nature entre ```null``` et ```undefined```. Si ces deux deux types expriment le vide mais :

- Dans le cas de ```null``` la variable contient quelque chose, elle a été **assignée mais à un contenu vide**.

- Dans le cas de ```undefined```, la variable n'a pas encore été assignée (d'où l'absence de =) et on ne sais pas du tout ce qu'elle contient, **son contenu est "indéfini"**.

Pour l'instant dans la pratique, la différence entre ces deux types ne va vraiment avoir d'impact sur votre code, sachez simplement qu'elle existe. Elle prendra plus de sens quand vous commencerez à travailler avec les objets et le DOM.

## 3\.Sources

- http://www.tutorialsteacher.com/javascript/javascript-null-and-undefined

- http://stackoverflow.com/questions/5101948/javascript-checking-for-null-vs-undefined-and-difference-between-and
