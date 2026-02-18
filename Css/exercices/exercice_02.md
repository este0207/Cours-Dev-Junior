# Consigne : 

Travaillez sur le même fichier `style.css`. L'objectif est de structurer la page et de gérer les états interactifs.

## Exercice 1 : Navigation et États 

- **Puces** : Supprimez les puces par défaut de la liste `.nav-list`.
- **Liens** : Stylisez les liens `<a>` à l'intérieur de la navigation pour qu'ils ne soient pas soulignés par défaut (`text-decoration`).
- **Lien Actif** : Ciblez le lien qui possède la classe `.active` pour lui donner une couleur différente et une bordure sous le texte.
- **Focus** : Ajoutez une règle `:focus` sur les liens pour qu'un contour épais apparaisse lorsqu'on navigue avec la touche TAB.

## Exercice 2 : Positions et Rang (Nth-child)

- **Alternance** : Dans la section `#features`, ciblez les `.card`. Coloriez le bord gauche de la 1ère et de la 3ème carte en bleu, et la 2ème en orange en utilisant `:nth-child()`.
- **Sélection précise** : Ciblez le deuxième lien du menu sans utiliser de classe, uniquement avec un sélecteur de position.
- **Réflexion** : Si j'ajoute un titre `<h2>` au tout début de ma section `#features`, est-ce que `.card:nth-child(1)` ciblera toujours la première carte ? Pourquoi ? (Répondez en commentaire).

## Exercice 3 : Flexbox - Alignement et Menu

- **Menu Horizontal** : Transformez la balise `ul.nav-list` en conteneur Flexbox pour aligner les éléments horizontalement.
- **Répartition** : Utilisez `justify-content` pour centrer le menu dans l'en-tête.
- **Boutons** : Ciblez la `div.actions` dans le Hero. Utilisez Flexbox pour aligner les deux boutons côte à côte avec un espace (gap) de 15px.

## Exercice 4 : Grid - La Grille de Cours

- **La Grille** : Ciblez la section `#features`. Transformez-la en grille (grid) avec 3 colonnes de largeur égale en utilisant l'unité `1fr`.
- **Espacement** : Ajoutez un gap de 30px pour que les cartes ne se touchent pas.
- **Adaptation** : Modifiez la grille pour qu'elle n'ait que 2 colonnes au lieu de 3. Que se passe-t-il pour la troisième carte ?

## Exercice 5 : Logique et Exclusion

- **Exclusion** : Donnez une opacité de 0.6 à toutes les cartes, SAUF celle qui a le statut `data-status="current"`, en utilisant la pseudo-classe `:not()`.
- **Le Vide** : Ciblez le paragraphe `<p>` vide dans la carte JavaScript. Utilisez `:empty` pour le cacher complètement (`display: none`) afin qu'il ne crée pas d'espace inutile.
- **Formulaire** : Ciblez l'input qui est `required` (obligatoire) et donnez-lui une petite bordure rouge à gauche pour le signaler à l'utilisateur.
