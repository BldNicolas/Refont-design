# Projet refont sémantique

Voici un projet qui a pour but de **comprendre les intérêts** de faire un code avec des **balises sémantiques** et qui respecte la **norme W3C**.

## Avantages

Voici les **intêrets** d'utiliser un **code sémantiquement** correct plutôt qu'un code remplis de ```<div>``` :
- **Meilleur compréhension** par le web : la navigation et la compréhension est facilitée pour les utilisateurs. Les éléments HTML sémantiques tels que `<header>`, `<nav>`, `<article>`, `<footer>`, etc., ont un rôle défini qui **aide à clarifier** la structure du document pour les lecteurs d'écran.
- **Meilleur référencement** : comme le contenue est mieux compris par les navigateurs, le **classement** du site Web est donc meilleur dans les résultats de recherche.
- **Maintenance** plus facile : le code est plus facile à comprendre, donc il est plus facile à **maintenir à jour**.
- **Facilité de style** : permet de ne pas utiliser de classe en css. **Simplifie** donc la conception et le formatage.
- **Utilisation appropriée pour tout le monde** : les technologies d'assistance **comprennent mieux** avec une sémentique bien définie.

## Description des changements

### Head

Dans le **Head**, nous ajoutons les balises méta qui permetteront de :
- **spécifier l'encodage** de caractères utilisé
```html 
<meta charset="UTF-8">
```
- rendre le site web **réactif** et **adapté** aux différents appareils
```html 
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- afficher un **extrait** de la page dans les résultats de recherche
```html 
<meta name="description" content="Cours de design et de codage">
```
- utiliser le **mode de rendu** le plus récent et le plus **compatible** avec les normes actuelles
```html 
<meta http-equiv="x-ua-compatible" content="IE=edge">
```
Nous ajoutons aussi les **icônes** qui seront utilisées lorsqu'un utilisateur ajoutera le site web à l'écran d'accueil
```html 
<link rel="apple-touch-icon" sizes="180x180" href="favicon/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="favicon/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="favicon/favicon-16x16.png">
<link rel="manifest" href="favicon/site.webmanifest">
<link rel="stylesheet" href="./css/screen.css">
```

### Body

Le code étant majoritairement composé de `<div>`, nous allons **remplacer** certaines balises.

| Code de base  | Sémantique | Justification |
| ------------- | ------------- | -------------- |
| `<div class="main">` | `<main class="main">` | Indique que le contenue est la **section principal** de la page |
| `div class="icon">` | `<div class="icon" role="img">` | Améliore l'**accessibilité** de la page web en renseignant le **role** de cette section |
| `<div class="menu">` | `<nav class="menu">` | Indique que le contenue représente un **menu navigable** |
| `<div class="search">` | `<form action="#" method="get" class="search">` | Permet l'**utilisation d'un input** en utilisant la méthode **get** |
| `<a href="#"> <button class="btn">Search</button></a>` | `<button class="btn">Search</button>` | On ne met pas un `<button>` dans un `<a>` |
| `<div class="content">` | `<section class="content" role="main">` | **Ajoute le rôle** `main` dans la section comprenant le **texte principale** de la page |
| `<button class="cn"><a href="#">JOIN US</a></button>` | `<form action="#" method="get"> <button class="cn">JOIN US</button> </form>` | Permet l'utilisation d'un input en utilisant la méthode **get** |
| `<div class="form">` | `<form action="#" method="get" class="form">` | Permet l'utilisation d'un input en utilisant la méthode **get** |
| ` <a href="#">Sign up </a> here</a></p>` | `<a href="#">Sign up </a>here</p>` | Enlève un `</a>` en trop |
| `<div class="icons">` | `<div class="icons" role="group">` | Ajoute un rôle pour améliorer l'accessibilité |
    
### CSS

Nous avons aussi **changer les unités** du CSS de `px` à `rem`, car cela offre plusieurs avantages, notamment la **scalabilité** basée sur la taille de police de l'élément racine, une meilleure **accessibilité** pour les utilisateurs qui modifient la taille de police, une **cohérence visuelle** sur divers appareils, une **facilité de maintenance** accrue et une **recommandation** en tant que meilleure pratique pour la conception web moderne.