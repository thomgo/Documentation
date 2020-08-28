# Ecrire du CSS

Voilà vous connaissez les bases de CSS, il grand temps maintenant de mettre en forme notre première page HTML. Pour cela voyons un peu plus en détails la syntaxe de CSS.

## 1\.Syntaxe détaillée

Reprenons une règle CSS basique et décortiquons la

```
p {
font-size: 20px;
font-style: italic;
}

```
**A\.Le sélecteur**

Comme nous l'avions expliqué ```p``` permet de cibler ou sélectionner tous les paragraphes ``` <p></p> ```de nos pages HTML. On dit par conséquent que ```p``` est notre sélecteur. **Une règle CSS commence toujours par un sélecteur **car nous devons savoir à quel élément elle s'applique.

Bien souvent votre sélecteur sera un élément HTML, pour écrire votre sélecteur il vous suffit de reprendre la balise HTML concernée et de lui retirer ses chevrons, ainsi pour sélectionner ``` <p></p> ``` sur ma page HTML j'utilise ```p``` dans mon CSS. Pour cibler tous mes ``` <h1></h1> ``` j'utilise ```h1```.

**B\.Les propriétés et leurs valeurs**

Ensuite, entre les accolades vient ce que l'on appelle les propriétés. Ce sont elles qui indiquent précisément quel aspect de notre balise HTML est à modifier. **Chaque propriété possède une valeur** qui détermine comment notre HTML sera modifié. **Chaque ligne propriété/valeur se termine avec un point-virgule**

Ces valeurs peuvent prendre la forme de **texte**, dans notre exemple la propriété ```font-style``` a comme valeur ```italic```, autrement-dit on indique que la police sera en style italique. D'autres propriétés peuvent prendre des **valeurs numériques**, c'est le cas de la propriété ```font-size```. En effet il est logique d'indiquer la taille de notre police en pixels. Ici tous les textes de nos paragraphes feront donc ```20px``` de haut.

**C\.Différentes unités pour nos valeurs**

Les valeurs numériques peuvent s'exprimer avec plusieurs unités différentes. Dans le cas précédent notre unité était le pixel mais vous devez savoir qu'il en existe plein d'autres. Pour l'instant, nous allons voir très brièvement les **pourcentages** et les **em** mais nous reviendrons plus en détails sur les différentes unités et leur comportement dans un prochain chapitre.

- **Les pourcentages** sont principalement utilisés pour indiquer des tailles d'éléments ou des marges par rapport à la taille de leur contenair. Par exemple :

```
div {
  width : 100%;
  height: 40%;
}

```

- **Les em** sont principalement utilisés pour les tailles de police et les marges. Une police de taille standard pour la lecture a une taille de 1em, ainsi une police de 3em sera 3 fois plus grande qu'une police standard.

```
p {
  font-size: 1.5em;
}

```
Retenez ces unités et essayez de les utiliser dans les exercices qui vont suivre pour vous familiariser avec leur comportement. Nous vous les expliquerons en détails plus tard.

## 2\.Quelques propriétés standard

Voici quelques unes des nombreuses propriétés CSS qui vous permettent par exemple de formater votre texte. Retenez-les bien, elles vous aideront à réaliser l'exercice qui arrive ! Pour voir l'ensemble des valeurs qui peuvent leur être assignées vous devrez aller consulter la documentation de MDN.

** A\.font-style**

Elle permet de styliser votre texte, elle peut prendre plusieurs valeurs comme "italic" par exemple.

**B\.font-size**

Elle permet de gérer la taille de vos textes ou de vos titres, elle prend une valeur numérique bien souvent en pixels ou en em.

**C\. font-weight**

Elle permet de gérer l'épaisseur de trait de votre texte. Cette propriété peut prendre des valeurs numériques (100, 200, 400...) ou une valeur sémantique telle que "bold" qui mettra votre texte en gras.

**D\.text-align**

Elle permet de gérer l'alignement du texte, à gauche, à droite ou au centre de son container.

**E\. text-decoration**

Elle permet par exemple de souligner ("underline") le texte ou encore de le barrer.

## 3\.Sources

- https://developer.mozilla.org/fr/Apprendre/CSS/Les_bases/La_syntaxe
