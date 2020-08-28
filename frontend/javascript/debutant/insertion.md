# Appliquer son JavaScript dans des pages HTML

Vous devez vous en doutez, nous ne faisons pas du JavaScript simplement pour le plaisir, tout l'intérêt est de l'intégrer à nos pages HTML afin de pouvoir dynamiser notre site. Comme pour le CSS, nous avons plusieurs méthodes à disposition pour l'intégration du JavaScript

## 1\.Où insérer le JavaScript ?

Nous vous avons dit que l'intégration de JavaScript dans nos pages ressemble à celle de CSS. Comme vous le savez nous intégrons le CSS dans la balise ```<head>``` de nos pages, soit en haut du document.

Vous pouvez très bien intégrer votre JavaScript dans l'en-tête de vos pages cependant vous vous exposerez à des problèmes. En effet, il est fréquent que **JavaScript travaille avec des éléments HTML** comme des images. Que se passera-t-il par exemple si notre code JavaScript modifie une image mais qu'au moment de l'exécution cette image n'est pas encore chargée ? Le code ne pourra pas être exécuté, voire pire provoquera un bug.

La solution à ce problème est très simple, **nous chargerons toujours nos fichiers JS en bas de page**, avant la fermeture de la balise ```<body>```. Cela nous assurera que l'ensemble du HTML a été chargé auparavant

## 2\.Insertion par la balise script

La première méthode pour insérer son code JavaScript dans ses pages est de le mettre **directement dans une balise** ```<script>``` avant la fermeture du body comme ceci :

```
<script type="text/javascript">
      alert("Salut les apprenants !");
    </script>
  </body>
</html>

```
Notez que l'attribut ```type``` n'est plus obligatoire, JavaScript étant reconnu par défaut par tout les navigateurs, vous n'avez pas besoin de préciser qu'il s'agit de JavaScript.

L'avantage de cette méthode est de nous permettre d'associer rapidement notre programme JavaScript aux éléments HTML correspondant puisqu'ils se trouvent sur la même page.

Cependant nous n'utiliserons cette méthode que pour de petits scripts. Autrement nos pages deviendraient vite **brouillonnent** et nous devrions **dupliquer notre code** sur toutes les pages où cela est nécessaire.

## 3\.Insertion avec un fichier JS séparé

Comme pour le CSS, **la meilleure méthode consiste à écrire tout notre JavaScript dans un fichier séparé**, cela permet de produire un code clair, facilement maintenable et réutilisable sur différentes pages.

Là encore le fichier s'insère grâce à la balise ```<script>````à laquelle on ajoute un attribut ```src``` contenant le chemin de notre fichier.

Dans l'exemple suivante je crée un lien vers le fichier main.js (nom d'usage de votre fichier JavaScript) qui se trouve au même niveau que notre fichier index.html. C'est ce fichier main.js qui contiendra notre message d'alerte.

index.html

```
<script type="text/javascript" src="main.js"></script>
  </body>
</html>

```
main.js

```
alert("Salut les apprenants !");

```

## 4\.Sources

- https://developer.mozilla.org/fr/Apprendre/HTML/Comment/Utiliser_JavaScript_au_sein_d_une_page_web

Faire exercice 05 "bienvenue dans la console" + 06 "Calculer mon age"
