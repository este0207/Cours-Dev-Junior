### Consigne : Utilisez uniquement votre fichier style.css. Ne modifiez pas le code HTML fourni.

## Exercice 1 : Le "Reset" et la Typographie

- **Le Body** : Ciblez l'élément `<body>` pour lui appliquer une couleur de fond `#f4f4f4` et la police de caractères sans-serif.
- **Titres** : Mettez tous les titres `<h3>` de la page en bleu marine (navy) et forcez-les à s'afficher en majuscules (via CSS) sans toucher au texte dans le HTML.
- **Sous-titre** : Ciblez le paragraphe qui a la classe `.subtitle` pour changer sa couleur en gris foncé (`#555`) et le mettre en italique.

## Exercice 2 : Maîtriser les Bordures et les États

- **Les Cartes** : Ajoutez une bordure de `2px solid #ddd` à tous les éléments ayant la classe `.card`.
- **Statut Spécial** : Ciblez spécifiquement la carte qui possède l'attribut `data-status="current"`. Changez sa bordure en `2px solid #007bff` (bleu) et donnez-lui un fond beige.
- **Réflexion** : Pourquoi le sélecteur `card { }` ne fonctionnerait-il pas pour styliser vos cartes ? Écrivez la réponse en commentaire dans votre fichier CSS.

## Exercice 3 : Espacement (Margin & Padding)

- **Sections** : Donnez à chaque section (`section`) un padding de `50px` en haut/bas et `20px` sur les côtés pour décoller le contenu des bords.
- **Navigation** : Ajoutez une marge de `20px` entre chaque élément de liste `<li>` dans votre menu de navigation (`.nav-list`).
- **Boutons** : Ciblez le bouton `.btn.primary` et augmentez son padding intérieur (`12px` haut/bas, `24px` gauche/droite) pour le rendre plus imposant que l'autre bouton.

## Exercice 4 : Relief et Interactivité

- **Ombres** : Appliquez aux trois `.card` une ombre de boîte (`box-shadow`) légère et un arrondi de coin (`border-radius`) de `10px`.
- **Survol** : Ajoutez un effet au survol (`:hover`) sur les cartes : l'ombre doit devenir plus sombre et la carte doit légèrement changer de couleur de fond.
- **Boutons** : Changez l'opacité des boutons (`button`) avec `opacity:` à `0.8` lorsqu'on passe la souris dessus.

## Exercice 5 : Ciblage Chirurgical et Formulaire

- **Le titre du Hero** : Ciblez uniquement le `<h1>` qui se trouve à l'intérieur de la section `#hero` pour augmenter sa taille de police (`font-size`).
- **Formulaire** : Ciblez l'input qui possède l'attribut `type="email"` et donnez-lui une bordure de couleur différente lorsqu'il est cliqué (état `:focus`).
- **Le Vide** : Ciblez le paragraphe `<p>` qui est vide (dans la carte JavaScript) à l'aide du sélecteur `:empty`. Donnez-lui une bordure rouge pointillée (`dotted`) de `1px` pour montrer qu'il manque du contenu.
