## 1\. Le concept de programmation orientée objet

### A\. La programmation orientée objet : définition et raison

Jusqu'à maintenant, vous avez fait ce que l'on appelle de la **programmation procédurale**. En résumé, vous écrivez vos instructions quand vous en avez besoin, l'ordinateur les lit dans l'ordre d'écriture et les exécute.

Au fil de vos développements procéduraux, vous avez dû remarqer que vous répétiez souvent du code, vous vous êtes alors mis à utiliser des fonctions pour rendre vos bouts de code facilement réutilisables. La programmation orientée objet va vous permettre d'aller encore plus loin dans la **réutilisabilité de votre code et son organisation**

Il s'agit d'un concept assez ancien de programmation qui pourtant est toujours d'actualité. En effet les développeurs qui vous ont précédés se sont rendus compte que plus les programmes grossissaient, plus ils étaient compliqués à maintenir, c'est alors qu'ils ont introduit le POO.

Elle se base sur un concept simple, **en POO tout doit être objet**

Mais un objet c'est quoi ? En fait c'est un **objet comme ceux que vous connaissez dans le monde réel**.

Prenons un objet que vous connaissez tous comme une ampoule par exemple. Cette ampoule possède deux choses :

- Des caractéristiques (être en verre par exemple)

- Des fonctionnalités (faire de la lumière par exemple)

Un objet en POO fonctionne exactement de la même manière, il possède des **caractéristiques** particulières et peut réaliser des **actions** pour nous.

Voyons maintenant concrètement comment tout ça se présente en JavaScript. Retenez bien tous ces concepts ils vous seront utiles en PHP et dans d'autres langages de programmation.

### B\. Un objet en JavaScript qu'est ce que c'est ?

Il faut voir les objets en JavaScript un peu comme des supers variables ou des supers tableaux. Ce sont des **containers améliorés** qui peuvent stocker aussi bien des données que des fonctions et ce sans limite de nombre.

Dorénavant quand vous aurez plusieurs variables qui se rapportent à un même élément (un utilisateur par exemple) il vous faudra créer un objet pour regrouper toutes ces variables.

Cela rendra votre code plus propre et plus facilement réutilisable par quelqu'un d'autre. Il en va de même pour vos fonctions qui se rapporteraient à cet utilisateur.

En programmation orientée objet, il faut retenir deux termes :

- **propriété**, c'est une donnée stockée dans un objet, c'est l'équivalent d'une variable

- **méthode**, c'est une fonction stockée dans un objet

## 2\.Comment créer un objet simple et l'utiliser ?

L'heure est venue de créer votre premier objet JavaScript et comprendre concrètement comment tout cela fonctionne. Sans plus attendre, voilà un objet très simple :

```
var homme = {
  nom: "Dupont",
  age: 45,
  getName: function() {
    alert(this.nom);
  }
};

```

Pour comparaison, voilà le code similaire mais en programmation procédurale :

```
var hommeName = "Dupont;
var hommeAge = 45;

function getHommeName() {
  alert(hommeName);
}

```

Vous remarquez plusieurs choses :

- pour créer un objet on déclare une variable classique mais avec des accolades de cette manière ```var homme = { contenu de l'objet };```. **Attention n'oubliez pas le point virgule à la fin.**

- chaque donnée ou fonction est indexée avec un nom. Dans notre exemple nous avons donc un integer (45) qui est identifié par l'index age. Donnez des index cohérents à vos données et à vos fonctions, autrement vous allez vous y perdre.

- chaque déclaration de méthode ou propriété se termine par une virgule, sauf la dernière (un peu comme dans un tableau)

- une méthode (ici getName) s'écrit comme une fonction anonyme classique

- ```this``` renvoie à l'objet lui même, ainsi la méthode getName alerte le nom de l'objet.

Bon déclarer des objets c'est bien mais s'en servir c'est encore mieux ! Maintenant que nous avons stocké plein de données dans notre objet, comment pouvons-nous nous en servir ?

Pour récupérer une propriété d'un objet, il suffit d'utiliser la syntaxe suivante :
- **objet.index**;

Ainsi si nous voulons afficher l'âge de notre homme, nous pouvons simplement écrire :

```
alert(homme.age);

```

Si nous voulons afficher le nom de notre homme, nous pouvons encore faire mieux et simplement appeler la méthode getName() qui alertera le nom de l'objet.

```
homme.getName();

```

**Attention n'oubliez pas les () car il s'agit d'une fonction**

Vous pouvez très simplement redéfinir les propriétés/méthodes de votre objet, un peu comme vous le faites pour une variable en utilisant la syntaxe suivante :

objet.propriété = nouvelle valeur;

Ainsi si vous souhaitez changer le nom de notre objet homme vous pouvez écrire :

```
homme.nom = "Martin";

```

Si vous rappelez la méthode getName() de notre objet, elle vous renverra "Martin" maintenant.

Cette syntaxe vaut également si vous souhaitez ajouter une propriété/méthode à votre objet, ainsi dans l'exemple suivant, nous ajoutons une propriété lieu avec une ville à notre objet homme :

```
homme.lieu = "Roubaix";

```

## 3\.Utiliser le constructeur d'objet

Vous savez maintenant déclarer des objets, leur assigner des propriétés, des méthodes et les modifier ce qui est déjà plutôt bien.

Précédemment nous avons créer un objet homme avec des caractéristiques particulières, mais que se passerait-t-il si dans notre programme nous devions interagir avec des dizaines d'objets homme, chacun ayant ses propres caractéristiques ?

Il faudrait alors réécrire chaque objet avec ses propriétés et ses méthodes. Bref ce serait répéter beaucoup de code pour rien. Le plus simple serait de pouvoir définir une sorte de modèle ou de schéma de l'objet homme sur la base duquel nous pourrions créer autant d'objets que nous voulons.

Devinez quoi petits chanceux que vous êtes, JavaScript vous offre cette possibilité ! En fait jusqu'à maintenant vous avez fait une déclaration **littérale** de vos objets, dorénavant vous aller utiliser le **constructeur**.

Le constructeur est en fait une fonction qui permet de définir un **prototytpe** pour notre objet. Si nous voulions créer un constructeur pour notre objet Homme, il se présenterait de la manière suivante :

```
function Homme (nom, age) {
  this.nom = nom;
  this.age = age;
  this.getName = function() {
    alert(this.nom);
  };
}

```

Cette fonction en elle-même ne fait rien, mais elle nous permet maintenant de créer autant d'homme que nous voulons avec chacun leurs propres caractéristiques.

En fait, ce petit bout de code dit qu'à chaque fois que nous appellerons la fonction Homme(), le premier paramètre sera le nom, le second sera l'âge. Ces deux propriétés seront chacune assignées à l'objet et une méthode sera ajoutée pour alerter le nom.

Nous pouvons maintenant déclarer deux objets Homme en utilisant notre constructeur fraîchement créé :

```
var homme1 = new Homme("Dupont", 45);

var homme2 = new Homme("Martin", 26);

```

Nous disposons maintenant de deux objets Homme différents, l'un s'appelant Dupont et l'autre Martin.

La syntaxe pour créer un objet à partir du constructeur est assez simple, il faut juste :

- Une variable où stocker l'objet que vous aller créer

- le mot clef new

- le nom du constructeur

- Les arguments que nous lui passons

var variabledestockage = new constructeur(argument);

Si l'on souhaitait alerter leurs noms à l'écran on pourrait accéder à leur méthode getName() de la manière suivante :

```
homme1.getName();
homme2.getName();

```

Il est bien évidemment possible de modifier notre objet à posteriori et lui rajouter des propriétés qu'il ne possédait pas au départ. Pour cela, vous utiliserez la syntaxe déjà vu dans les déclarations littérales d'objets.

Ainsi pour ajouter une propriété taille à notre objet, nous pouvons écrire :

```
homme1.taille = 184;

```
