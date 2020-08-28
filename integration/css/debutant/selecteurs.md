# Aller plus loin avec les sélecteurs

Nous avons déjà abordé rapidement le cas des sélecteurs lorsque nous avons réalisé notre première feuille de style. Il reste pourtant beaucoup à dire à leur sujet, nous sommes loin d'avoir vu tous les types de sélecteurs et comment les utiliser.

## 1\.Les éléments

Il s'agit du **sélecteur le plus basique** que nous avons déjà rencontré. Souvenez-vous, il s'agissait par exemple de "p" pour sélectionner les balises ``` <p></p> ```.

Comment faire cependant si ne voulons pas cibler tous les paragraphes avec notre règle mais seulement certains en particulier ? Grâce à la magie de CSS il est possible d'être plus précis et de **sélectionner un élément à l'intérieur d'un autre.**

Par exemple je peux sélectionner uniquement les paragraphes qui sont à l'intérieur d'une balise ``` <nav> ```:

```
nav p {
  font-style: italic;
}

```

Je peux rajouter des éléments de cette manière à l'infini, ainsi je peux ne sélectionner que les ``` <p> ``` qui sont à l'intérieur d'une ``` <nav> ``` qui est est elle-même à l'intérieur d'un ``` <header> ```.

Que faire si je veux que ma règle s'applique à plusieurs éléments différents ? Je ne vais pas réécrire deux fois la même règle, je peux simplement mettre **plusieurs sélecteurs séparés par une virgule**. Ici j'applique un fond bleu à ma balise ``` <nav> ``` et à ma balise ``` <header> ```.

```
nav, header {
  background-color: blue;
}

```
## 2\.Les classes

Il s'agit là d'un sélecteur un peu particulier qui va de paire avec les ID que nous verrons juste après. Ce sélecteur permet de cibler tous les éléments HTML possédant la classe en question. L'avantage est de pouvoir définir un style commun que l'on pourra très facilement appliquer à différentes balises HTML en leur ajoutant juste la class nécessaire.

Les classes sont donc un des **sélecteurs les plus utilisés en CSS** et vous ne pourrez bientôt plus vous en passer. En CSS la classe se cible avec ``` .nomdeclasse ```. Pour appliquer un fond bleu à tous les éléments portant la classe "prix" je peux écrire :

```
.prix {
  background-color: blue;
}

```

## 3\.les ID

Les ID ont un fonctionnement similaire aux classes à la différence que leur utilisation est unique. En effet on ne peut pas retrouver deux fois le même ID sur une page HTML.

Les règles relatives à un ID ne ciblent donc qu'un seul élément. l'ID est par conséquent un **sélecteur extrêmement précis qui s'utilise en dernier recours**. Il est appelé avec ``` #nomdelid ```.

Par exemple pour appliquer une couleur à l'élément portant l'ID prix :

```
#prix {
  background-color: blue;
}

```

## 4\.Le sélecteur universel

Il s'agit d'un sélecteur qui comme son nom l'indique permet de cibler tous les éléments de la page. Il s'utilise avec * au début du fichier CSS pour des règles très générales et notamment pour supprimer le formatage appliqué par défaut sur certains navigateurs.

Par exemple, une pratique commune est de supprimer toutes les marges (nous verrons de quoi il s'agit plus tard) sur tous les éléments pour les remettre à 0 :

```
* {
  margin: 0;
  padding: 0;
}

```

## 5\.Sources

- http://www.w3schools.com/cssref/css_selectors.asp
