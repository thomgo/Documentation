# Les couleurs

Bon le chemin parcouru jusqu'à maintenant est déjà très bien, vous avez appris beaucoup de choses mais je trouve que nos pages web sont un peu tristes. Tout cela manque un peu de couleurs

Les couleurs sont un élément essentiel de la mise en forme CSS, en effet une charte graphique moderne et agréable à l'oeil vous assurera souvent un plus grand nombre de visites sur votre site.

En css vous disposez de trois solutions pour indiquer une couleur :

- **Ecrire directement le nom de votre couleur**, par exemple "red". Les navigateurs modernes en connaissent normalement 140.

- **Utiliser une notation hexadécimale** à 6 chiffres ou lettres, le code hexadécimal de la couleur rouge est "FF0000" par exemple. Chaque couple de digit correspond aux proportions de rouge, de vert et de bleu, offrant ainsi des milliers de nuances.

- **Utiliser la notation RGB** qui indique les proportions de rouge, de bleu et de vert avec des chiffres allant de 0 à 255. Rouge s'écrit ainsi "255, 0, 0"

Les couleurs peuvent s'utiliser avec de nombreuses propriétés mais nous en retiendrons deux principales :

- **color** qui modifie la couleur du texte

- **background-color** qui modifie la couleur de fond

Exemple :

Je souhaite écrire en rouge dans mes paragraphes

```
p {
  color: #ff0000;
}

```

Je souhaite que le fond de mes paragraphes soit rouge (couleur en mode rgb)

```
p {
  background-color: rgb(255, 0, 0);
}

```
![couleurs en css](illustrations/couleurs-css.jpg)

En pratique **les notations que vous utiliserez le plus seront les notations hexadécimales et RGB** afin de pouvoir profiter des milliers de nuances offertes par CSS.

Vous pouvez utiliser des outils en ligne tels que http://colorschemedesigner.com/csd-3.5/ afin de récupérer les codes couleur.
