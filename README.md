# Workshop : Créer un Dashboard Moderne et Réactif en HTML/CSS/JS

## Objectif:
Créer un dashboard interactif et esthétique qui consomme les APIs définies dans le premier workshop (**C#/Django/HTML-CSS-JS**). Chaque API implémentée correspond à un exercice du premier workshop.

## Pré-requis:
- Avoir installé: apache2
Fedora:
```sh
dnf install apache2
```
Ubuntu:
```sh
apt-get install apache2
```

---

## Plan du Workshop

### Introduction:
- **But** : Étendre le premier workshop en créant une interface utilisateur réactive et visuelle.

Vous travaillerez dans le dossier `/var/html/www/`
On vous suggère d'ouvrir VSCode directement dans ce dossier.

---

## Exercices

### **Exercice 1 : Préparer la structure de base**
**Objectif :** Mettre en place le squelette du dashboard avec une barre latérale gauche et une zone de contenu principal.

#### Étapes :
1. **Créer les fichiers** : `index.html`, `style.css`, `script.js`.
2. **Structure HTML** :
   - Ajouter une barre de navigation horizontale (`<header>`).
   - Créer une barre latérale gauche (`<nav>`) pour le menu des onglets.
   - Inclure une zone de contenu principal (`<main>`).
3. **Liens CSS et JS** :
   - Ajouter un `<link>` pour le CSS.
   - Ajouter un `<script>` avec l’attribut `defer`.

#### Indication :
- La barre latérale doit contenir un conteneur pour des onglets dynamiques (`<ul id="sidebar-menu">`).
- Les IDs des sections doivent être explicites, par exemple, `id="content"` pour la zone principale.

---

### **Exercice 2 : Styliser le Dashboard**
**Objectif :** Créer un design moderne et responsive.

#### Étapes :
1. **CSS Grid pour la disposition** :
   - Divisez la page en trois zones principales : `header`, `nav`, et `main`.
   - Utilisez `grid-template-areas` pour la disposition.
2. **Styles modernes** :
   - Appliquez des couleurs neutres ou pastel.
   - Ajoutez des ombres douces et des coins arrondis pour un effet visuel moderne.
3. **Responsive design** :
   - Ajoutez des media queries pour transformer la barre latérale en menu déroulant sur mobile.

#### Indication :
- Pour la barre latérale, utilisez une largeur fixe en desktop (ex. : `250px`) et transformez-la en menu caché sur mobile.
- Les transitions CSS (`transition: all 0.3s ease;`) amélioreront l'expérience utilisateur.

---

### Exercice 3 : Implémenter l'API "Addition de deux entiers"
**Objectif :** Créer un onglet dans la barre latérale pour l’API "Addition de deux entiers" et afficher un formulaire dans la zone principale.

#### Étapes :
1. **Créer un onglet** :
   - Ajouter un élément de menu dans la barre latérale (`<li>Calculatrice</li>`).
   - Utilisez JavaScript pour détecter les clics et afficher la section correspondante.
2. **Créer le formulaire** :
   - Inclure deux champs `<input>` pour les entiers et un bouton `<button>` pour soumettre.
   - Ajoutez un conteneur pour afficher le résultat.
3. **Connecter à l’API** :
   - Utilisez `fetch()` pour envoyer les deux entiers à l’API et afficher le résultat dans la zone principale.

#### Indication :
- La fonction JS pour soumettre les entiers pourrait s’appeler `submitAddition()`.
- Gérez les erreurs d’entrée utilisateur (par exemple, si un champ est vide).

---

### Exercice 4 : Implémenter l'API "Liste des publications"
**Objectif :** Créer un onglet pour récupérer et afficher les publications via l'API.

#### Étapes :
1. **Créer un onglet** :
   - Ajouter un nouvel élément dans la barre latérale (`<li>Publications</li>`).
   - Utilisez JS pour afficher les données dans la zone principale au clic.
2. **Faire la requête API** :
   - Utilisez `fetch()` pour récupérer les données des publications.
Assurez-vous d'utiliser async/await et d'être à l'aise avec ce concept en Javascript. Voici une source pour vous aider à faire de la programmation asynchrone : [cliquez-ici](https://medium.com/@francesco.saviano87/mastering-javascript-promises-and-async-await-8a5c1921b11a#:~:text=The%20async%20keyword%20is%20used,code%2C%20improving%20readability%20and%20maintainability.)
   - Transformez les données JSON en éléments HTML dynamiques.
3. **Afficher les publications** :
   - Créez une carte (`<div class="card">`) pour chaque publication avec un titre et un extrait.

#### Indication :
- Utilisez `document.createElement()` pour générer les cartes dynamiquement.
- Ajoutez une fonction `renderPosts(data)` pour organiser l’affichage.

---

### Exercice 5 : Implémenter l'API "Créer une publication"
**Objectif :** Ajouter un onglet pour soumettre une nouvelle publication.

#### Étapes :
1. **Créer un onglet** :
   - Ajouter un nouvel élément dans la barre latérale (`<li>Créer une publication</li>`).
   - Affichez un formulaire avec un champ `titre` et un champ `contenu`.
2. **Envoyer les données à l’API** :
   - Utilisez `fetch()` avec la méthode POST pour envoyer les données JSON.
   - Affichez un message de confirmation après succès.

#### Indication :
- La fonction pour envoyer les données pourrait être `submitPost()`.
- Ajoutez une gestion d’erreurs pour les réponses invalides de l’API.

---

### Exercice 6 : Implémenter l'API "Str_to_word_array"
**Objectif :** Ajouter un onglet pour tester l’API "Str_to_word_array".

#### Étapes :
1. **Créer un onglet** :
   - Ajouter un élément de menu (`<li>Str_to_word_array</li>`).
   - Affichez un champ `<textarea>` pour entrer un texte.
2. **Connecter à l’API** :
   - Utilisez `fetch()` pour envoyer le texte à l’API et afficher le tableau résultant.
3. **Afficher les résultats** :
   - Affichez les mots sous forme de liste ordonnée (`<ol>`).

#### Indication :
- Ajoutez une gestion des erreurs si l’entrée est vide ou si l’API échoue.
