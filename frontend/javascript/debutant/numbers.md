# Les nombres en JavaScript

Nous avons déjà parlé du type number dans un chapitre précédent et si à priori il se comprend plutôt facilement, il y a encore beaucoup à dire à son sujet.

Vous n'avez absolument pas besoin d'être bon en maths pour faire du JavaScript mais vous devez quand même savoir quelques petites choses sur les nombres.

## 1\.Les nombres: bases

Comment reconnaître une donnée de type number ? En fait c'est très simple, il s'agit d'un nombre écrit au format numérique. Souvenez-vous voilà les exemples qui avaient été donnés précédemment :

```
4

5.36

-45

```
On peut en déduire une chose très importante, à la différence d'autres langages, il n'y a qu'un seul type pour les nombres, à savoir number. JavaScript ne fait pas la différence entre les chiffres, les nombres et les nombres à virgule.

**Attention !** deux erreurs très courantes sont de:

- **Mettre ses nombres entre guillemets** mais ```"4"``` et ```4``` sont deux choses différentes en JavaScript. Le premier sera considéré comme du texte alors que le second sera considéré comme un nombre.

- **Utiliser une virgule** pour les nombres à virgule. En JavaScript il faut utiliser un point.

## 2\.Allons plus loin avec les nombres

Il reste encore beaucoup à dire sur les nombres en JavaScript, les concepts qui suivent sont importants mais pour l'instant vous devez juste savoir qu'ils existent, pas besoin de les connaître par coeur :

- **La précision**: petit détail qui peut avoir son importance, Javascript perd en précision avec les nombre comportant plus de 15 chiffres. Au delà, ils peuvent être arrondis à l'unité supérieure.  

- **NaN**: Il s'agit d'une expression qui signifie "not a number" il se peut que cette valeur vous soit retournée lors d'une opération qui n'est pas valide, c'est le cas par exemple de ```0/0```

## 3\.Que faire avec nos nombres ?

Comme avec les chaînes de caractères, on peut faire beaucoup de choses avec nos nombres parmi lesquelles :

- Des opérations mathématiques

- Assigner des positions

- Assigner des valeurs

- Effectuer des comparaisons

- Et plein d'autres choses....

## 4\.Sources

- http://www.w3schools.com/js/js_numbers.asp

- https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Objets_globaux/Number

- https://fr.wikipedia.org/wiki/NaN
