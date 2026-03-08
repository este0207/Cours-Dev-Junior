# C'est quoi le "Utility-First" ?

D'habitude, tu fais ça :

```html
<button class="btn-bleu">Clique moi</button>
```

```css
.btn-bleu { 
    background-color: blue; 
    padding: 10px; 
    border-radius: 5px; 
}
```

Avec Tailwind, tu fais tout au même endroit :

```html
<button class="bg-blue-500 p-4 rounded-lg text-white">Clique moi</button>
```

## Pourquoi c'est génial ?

- **Vitesse** : Plus besoin de switcher entre HTML et CSS.
- **Maintenance** : Tu sais exactement quel style affecte quel élément.
- **Pas de noms bizarres** : Plus besoin de chercher si tu dois appeler ta div container-wrapper-inner-v2.

## Les bases de la syntaxe

Voici les classes les plus utilisées pour démarrer :

### Les Espacements (Margin & Padding)

Le chiffre (ex: 4) correspond à une unité de base (1 unit = 0.25rem, soit 4px par défaut).

- `p-4` : Padding partout.
- `mx-2` : Marge horizontale (gauche et droite).
- `mt-10` : Margin-top.

### Les Couleurs et Textes

- `text-red-500` : Texte rouge (le chiffre va de 50 à 950 pour l'intensité).
- `bg-slate-800` : Background gris foncé.
- `font-bold` : Texte en gras.
- `text-center` : Aligner le texte au centre.

### Le Layout (Flexbox)

Faire une mise en page devient un jeu d'enfant :

- `flex` : Active Flexbox.
- `items-center` : Aligne verticalement.
- `justify-between` : Espace les éléments au maximum.

## Le Responsive Design

C'est là que Tailwind brille. Au lieu d'écrire des `@media queries` complexes, tu ajoutes un préfixe :

- `w-full` : Largeur 100% par défaut (mobile).
- `md:w-1/2` : À partir des tablettes, passe à 50% de largeur.
- `lg:grid` : Sur grand écran, passe en mode Grille.

## Exemple Concret : Une carte de profil

```html
<div class="max-w-sm mx-auto bg-white rounded-xl shadow-md overflow-hidden p-6 border border-gray-200">
    <div class="flex items-center space-x-4">
        <div class="shrink-0">
            <div class="h-12 w-12 bg-indigo-500 rounded-full"></div>
        </div>
        <div>
            <div class="text-xl font-medium text-black">Apprendre Tailwind</div>
            <p class="text-slate-500">C'est rapide et efficace !</p>
        </div>
    </div>
    <button class="mt-4 w-full bg-indigo-600 text-white py-2 rounded-md hover:bg-indigo-700 transition">
        Commencer
    </button>
</div>
```

## Comment l'installer ?

Pour débuter sans se prendre la tête, tu peux ajouter ce script dans le `<head>` de ton fichier HTML (version CDN) :

```html
<script src="https://cdn.tailwindcss.com"></script>
```
