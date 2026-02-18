# Guide Ultime : Apprendre le CSS par la Pratique

Le CSS (Cascading Style Sheets) est le langage qui habille votre HTML. Pour réussir, il faut comprendre deux choses : Comment désigner un élément (le Sélecteur) et Quoi lui appliquer (la Règle).

## I. La Syntaxe et les Sélecteurs (Le "Qui")

Avant de peindre, il faut choisir son mur.

### 1. Les 3 Sélecteurs de base

- **Balise** : Cible tous les éléments d'un type.
    - `p { ... }` (tous les paragraphes).

    - **Erreur classique** : Écrire `btn { }` au lieu de `.btn { }`. Le navigateur cherche une balise `<btn></btn>`. Comme elle n'existe pas en HTML standard, rien ne se passe.

    - **Correction** : Utiliser `.btn { }` pour cibler l'attribut `class="btn"`

- **Classe (.)** : Cible les éléments avec une étiquette spécifique. Réutilisable.
    - `.btn { ... }` (tout ce qui a `class="btn"`). **Attention** : Ne jamais oublier le point . !

- **ID (#)** : Cible un élément unique.
    - `#main-nav { ... }` (l'élément avec `id="main-nav"`). **Attention** : Il n'existe qu'un id du même nom !

### 2. La Généalogie (Parent, Enfant, Descendant)

#### L'Espace : Le "Descendant" 

`#articles a` 
- Cible tous les liens présents dans la section articles, qu'ils soient dans un paragraphe, dans une liste de tags, ou dans le footer de l'article.

- **Exemple** : ici tous les `a` vont etre affecter.
```html
    <section id="articles">
        <a href="/">coucou</a>
        <p><a href="/">bonjour</a></p>
        <ul>
            <li><a href="/">Accueil</a></li>
            <li><a href="/about">À propos</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </section>
```

#### Le Signe `>` : L'Enfant Direct 

`.site-footer > a` ne cible que les liens qui sont "fils" du footer.

- **Exemple** : ici seul le premier `a` vas etre affecter car il est enfant direct de la class `.site-footer`
```html
    <div class="site-foter">
        <a href="/">coucou</a>
        <p><a href="/">bonjour</a></p>
    </div>
```

- **Pourquoi ça échoue souvent ?** Si ton lien est dans un paragraphe (`<footer><p><a>...</a></p></footer>`), alors le lien n'est plus l'enfant direct, c'est le petit-enfant. Le sélecteur `>` échouera. Il faudrait écrire `.site-footer p > a`.

#### Cibler un ID spécifique

L'ID (`#`) est prioritaire sur tout.

- **EX-3 :** Si tu écris `.contact`, ça ne marche pas car "contact" est un ID (`id="contact"`), pas une classe. Il faut écrire `#contact`.

```css
#contact {
    background-color: lightgray; /* Change la couleur de fond en gris clair */
}
```
- **Attention** : Il n'existe qu'un id du même nom !

## II. Les Propriétés de Style (Le "Quoi")

### 1. Couleurs et Texte

- `color` : Couleur du texte.
- `background-color` : Couleur du fond.
- `text-transform: uppercase;` : Met le texte en majuscules.

**Format des couleurs :**
- Nom : `red`
- Hexadécimal : `#ff0000`
- RGB : `rgb(255, 0, 0)`

```css
/* Exemple de style pour une class .btn */
.btn {
    background-color: blue; /* Couleur de fond */
    color: #ffffff;           /* Couleur du texte en blanc */
}
```

### 2. Le "Box Model" (Bordures, Marges, Remplissage)

Tout élément HTML est une boîte.

- **Border (Bordure)** : La ligne autour de l'élément.
    - `border: 3px solid black;` (Épaisseur, Style, Couleur).

- **Padding (Remplissage)** : L'espace intérieur (entre le texte et la bordure).

- **Margin (Marge)** : L'espace extérieur (pour éloigner les voisins).

![schema padding et margin](/public/padding-margin.png)

### 3. Effets Visuels : Box Shadow

Pour donner du relief :
```css
box-shadow: 5px 5px 10px rgba(0,0,0,0.5);
/* Décalage X, Décalage Y, Flou, Couleur */
```

## III. Position et Dynamisme (Les États)

### 1. Les Pseudo-classes de position

Indispensables pour styliser des listes sans ajouter des classes partout :

- `:first-child` : Le premier enfant.
- `:last-of-type` : Le dernier de son genre.
- `:empty` : Cible les éléments qui n'ont pas de contenu **(pas même un espace)**.
  
  - **Exemple :** Si tu veux cacher un élément vide, tu peux utiliser ce sélecteur.
  
  ```css
    .container :empty {
        display: none; /* Cache les éléments vides */
    }
  ```
  ```html
    <div class="container">
        <div>Contenu 1</div> <!-- Pas celle ci -->
        <div></div> <!-- Cette div vide sera caché -->
        <div>Contenu 2</div> <!-- Pas celle ci -->
        <div></div> <!-- Cette div vide sera également caché -->
    </div>
  ```
- `:nth-child(2)` : Le deuxième précisément.
- `:nth-child(even)` : Tous les éléments pairs (2, 4, 6...).

- **Le piège du type :** Si tu écris `#articles :nth-child(2)`, tu demandes le 2ème enfant de la section. Mais attention, le 1er enfant est souvent un `<header>`. Donc le 2ème enfant n'est pas forcément le 2ème `<article>`, c'est peut-être le premier !

- **Solution :** Utiliser `:nth-of-type(2)` qui ne compte que les éléments de même nom.

### 2. L'Interactivité (Clavier & Souris)

- `:hover` : Quand la souris survole l'élément.
- `:focus` : Quand l'élément est sélectionné au clavier (Tab).

## IV. Les Relations entre Voisins (Sisters)
### 1. Le voisin immédiat (`+`)

- `h2 + p` : Cible le paragraphe seulement s'il touche directement le `h2`. S'il y a une `div` entre les deux, ça ne marche plus.

- **Exemple :** Ici tout les `p` sont affecter.

```html
    <style>
        h2 + p {
            color: blue;
            font-weight: bold;
        }
    </style>
    <body>
        <h2>Titre de la section</h2>
        <p>Ceci est un paragraphe qui suit directement le h2.</p>
        
        <div>
            <h2>Un autre titre</h2>
            <p>Ceci ne sera pas affecté car il est dans une div.</p>
        </div>
        
        <h2>Encore un titre</h2>
        <p>Ceci est un autre paragraphe qui suit directement le h2.</p>
    </body>
```


### 2. Le voisin général (`~`)

- `.title ~ .lead` : Cible tous les `.lead` qui suivent un `.title`, même s'il y a d'autres balises entre eux.

- **Exemple :** Ici tous les `.lead` qui suivent un `.title` sont affecter.

```html
<body>
    <div class="title">Titre Principal</div>
    <p>Un paragraphe entre les deux.</p>
    <div class="lead">Texte d'introduction qui suit le titre.</div>
    <p>Un autre paragraphe.</p>
    <div class="title">Un Autre Titre</div>
    <div class="lead">Texte d'introduction qui suit le deuxième titre.</div>
</body>
```


##  Résumé 

| Si tu veux cibler... | Utilise... | Pourquoi ? |
|---|---|---|
| Un ID | `#nom-id` | L'ID commence par un hashtag. |
| Une classe | `.nom-classe` | La classe commence par un point. |
| Un élément vide | `:empty` | Pratique pour cacher des balises inutiles. |
| Le 2ème élément | `:nth-child(2)` | Le CSS compte à partir de 1. |
| Juste après un titre | `h2 + p` | Le signe + cible le voisin immédiat. |
| Tout sauf un élément | `:not(.classe)` | Pour exclure une exception. |

## Mini-Défi d'entraînement

Dans ton fichier `style.css`, essaye de réaliser ceci sans modifier le HTML :

- 1. Donne une bordure rouge à tous les articles, sauf au premier.
- 2. Fais en sorte que les liens du menu changent de couleur de fond au survol (`:hover`).
- 3. Cache tous les paragraphes qui n'ont pas de contenu.

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini-Défi d'entraînement</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#">Accueil</a></li>
                <li><a href="#">À propos</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <article>
            <h2>Titre de l'article 1</h2>
            <p>Contenu de l'article 1.</p>
        </article>
        <article>
            <h2>Titre de l'article 2</h2>
            <p></p>
        </article>
        <article>
            <h2>Titre de l'article 3</h2>
            <p>Contenu de l'article 3.</p>
            <p></p>
        </article>
    </main>
</body>
</html>
```