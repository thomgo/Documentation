#JQuery et le DOM#

Nous avons déjà abordé la notion de sélecteurs en analysant la syntaxe jQuery. **Les sélecteurs jQuery se basent sur le modèle des sélécteurs CSS**. Il est maintenant temps de revenir dessus plus en détails afin que vous puissiez accéder à l'ensemble du DOM.

Remarque : dans tous les exemples donnés, nous utiliserons la méthode .hide() qui permet de masquer un élément de la page. Il est conseillé, pour vous entraîner, de tester vous même le code dans vos fichiers.

##1\.Eléments##

Pour sélectionner les éléments HTML en jQuery, le principe est exactement le même qu'en CSS. Il suffit de **reprendre le nom de la balise** et de respecter la syntaxe jQuery.

Par exemple, si je veux sélectionner toutes les ``` <div> ``` de ma page et les cacher avec jQuery :

```
$( document ).ready(function() {
  $("div").hide();
});

```

##2\.Classe##

Là encore le principe est le même qu'en CSS, vous sélectionnez tous les éléments portant la classe concernée avec **".nomdeclasse"**.

Par exemple si je veux appliquer une méthode à tous les éléments de classe "wrapper" :

```
$( document ).ready(function() {
  $(".wrapper").hide();
});

```

##3\.ID##

Là encore le principe est le même qu'en CSS, vous sélectionnez un élément en particulier avec son id grâce à **"#nomdeid"**.

Par exemple si je veux appliquer une méthode à mon élément avec l'id "finished" :

```
$( document ).ready(function() {
  $("#finished").hide();
});

```

##4\.Allons plus loin dans nos sélections##

Nous avons vu les sélecteurs les plus classiques et vous pouvez déjà faire pas mal de choses sur vos pages web avec ce que vous savez. Toutefois, vous devez savoir que jQuery nous offre bien d'autres possibilités :

- **sélections multiples :** si votre instruction concerne plusieurs éléments, il est inutile de la réécrire à chaque fois. Vous pouvez les sélectionner en une fois en les séparant par une virgule.

Par exemple si je veux sélectionner mes titres et mes paragraphes :

```
$( document ).ready(function() {
  $("h1, p").hide();
});

```
- **sélection d'un élément dans un autre :** pour sélectionner uniquement mes balises ```<p>``` à l'intérieur de mes ```<div>``` je peux écrire comme en CSS :

```
$( document ).ready(function() {
  $("div p").hide();
});

```
- **sélecteur universel :** comme en CSS vous pouvez sélectionner tous les éléments sur la page à l'aide du sélecteur universel : ```*```

```
$( document ).ready(function() {
  $("*").hide();
});

```

- **pseudo-sélécteurs :** jQuery vous offre également un ensemble de sélecteurs hérités des pseudo-classes CSS. Il sont trop nombreux pour être nommés ici, vous devrez donc vous référez à la documentation (https://api.jquery.com/category/selectors/) pour tous les découvrir.

Je peux par exemple sélectionner uniquement le premier ```<p>``` rencontré dans le DOM avec ":first" :

```
$( document ).ready(function() {
  $("p:first").hide();
});

```

##5\.Sources##

- http://www.w3schools.com/jquery/jquery_selectors.asp

- https://api.jquery.com/category/selectors/
