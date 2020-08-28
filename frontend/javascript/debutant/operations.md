# Réaliser ses premiers scripts

Pour pouvoir réaliser vos premiers scripts, il y a quelques grandes notions que vous devez connaître. Vous verrez qu'elles vous permettront de faire des choses plutôt sympas avec JavaScript. Jetons y un coup d'oeil ensemble.

## 1\. Concaténer ses textes

Derrière ce mot un peu barbare se cache une chose très simple. En JavaScript, comme dans de nombreux langages de programmation, vous avez la possibilité de **mettre bout à bout deux chaînes de caractères pour n'en faire plus qu'une** en utilisant le symbole ```+```.

Cela vous permet de récupérer différents morceaux de texte pour n'en faire plus qu'un. La concaténation est donc idéale quand on reçoit les chaînes de caractères petit à petit et qu'il faut les afficher en une seule fois.

Un exemple sera plus parlant que des mots. Ici ma variable texte contiendra une seule string avec pour valeur "Bonjour mon ami"

```
var texte = "Bonjour" + " mon ami";

```

Je peux aussi **concaténer directement des variables de type string**, ici ma variable texte aura toujours la même valeur:

```
var a = "Bonjour";
var b = " mon ami";

var texte = a + b;

```

## 2\. Opérations mathématiques de base

JavaScript reconnaît également toutes les **opérations mathématiques** pour peu que les données soient du type number. Nous pouvons donc réaliser :

- Des additions (+)

- Des soustractions (-)

- Des multiplications (*)

- Des divisions (/)

- Et bien d'autres choses que nous verrons plus tard !

Nous pouvons par exemple afficher directement le résultat d'une addition à l'écran, ici nous afficherons 10 :

```
alert(8+2);

```

Nous pouvons stocker le résultat de nos calculs dans une variable et l'afficher par la suite, ici nous afficherons 4 :

```
var result = 8/2;
alert(result);

```

Nous pouvons également **effectuer des opérations directement sur les variables** pour peu qu'elles soient du type number, ici nous afficherons 20 :

```
var a = 10;
var b = 2;
alert(a*b);

```

Si jamais vous vous trompez et et essayez de réaliser une opération avec une string et un nombre comme dans le cas suivant, que se passera-t-il ?

```
var result = "4" + 4;

//ou

var result = "4" - 4;

```
Cela dépend, dans le cas de l'addition le signe ```+``` sera considéré comme une concaténation et ```result``` vaudra en fait 44. Dans le cas de la soustraction "4" sera converti en nombre par défaut et ```result``` vaudra 0.

Même si aucun bug n'est provoqué, **sachez qu'il s'agit d'une erreur**, vous ne devez pas réaliser des opérations sur des chaînes de caractères. La bonne pratique consiste à **convertir sa chaîne en nombre**. Il existe déjà des méthodes pour faire cela !

## 3\. Propriétés et méthodes

**A\. Propriétés**

Quand vous récupérez des données de différents types (string, number etc...), il y a des **propriétés associées à ces données**. Voyez les propriétés un peu comme des **opérations déjà enregistrées pour accéder à des informations spécifiques**. Les propriétés sont nombreuses, il faudra vous référez à la documentation pour les connaître.

Par exemple une des propriétés des données de type string est leur longueur. Autrement-dit on peut connaître la nombre de caractères contenu dans n'importe quelle chaîne en utilisant cette propriété.

La propriété en question est ```.length```. La syntaxe est la suivant :

```
string.length;

```

Dans l'exemple ci-dessous, j'affiche la longueur de ma variable test, soit 18. Si vous comptez les lettres et les espaces entre les guillemets vous verrez que vous arrivez effectivement à 18.

```
var test = "Une phrase de test";
alert(test.length);

```

**B\. Méthodes**

Les méthodes sont également **des opérations "pré-enregistrées"**  dans JavaScript qui permettent de réaliser de **nombreuses transformations sur les données**.

Les opérations réalisables vont de la modification d'un caractère particulier dans une chaîne à la suppression des décimales d'un nombre à virgule.

Là encore, vous ne pourrez jamais toutes les connaître, la documentation sera votre meilleure amie. Nous allons prendre une méthode pour l'exemple, celle qui permet de passer une chaîne de caractère en majuscules.

Notre méthode s'appelle ```.toUpperCase()```, elle s'utilise comme une propriété si ce n'est qu'il faut lui ajouter des parenthèses. Dans l'exemple suivant notre variable sera affichée tout en majuscules :

```
var test = "Une phrase de test";
alert(test.toUpperCase());

```
## 4\. Sources

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length

- http://www.w3schools.com/js/js_string_methods.asp
