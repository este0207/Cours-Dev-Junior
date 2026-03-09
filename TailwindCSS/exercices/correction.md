# Correction

## Exo 1 Le Carré de couleur

Pour faire un carré, il faut que la largeur `(w)` soit égale à la hauteur `(h)`.

```html
    <div class="w-32 h-32 bg-blue-500 rounded-lg"></div>
```

- `w-32` / `h-32` : taille moyenne (128px)
- `bg-blue-500` : Le bleu standard
- `rounded-lg` : Pour des coins bien arrondis mais pas circulaires

## Exo 2 Texte d'Alerte

Ici, on joue sur la typographie.

```html
    <p class="text-4xl font-bold text-yellow-500">
        Attention !
    </p>
```

- `text-4xl` : Très grand (36px)
- `font-bold` : Pour l'épaisseur du trait
- `text-yellow-500` : La couleur vive pour l'alerte

## Exo 3 Le Buy Button (+ Bonus Hover)

C'est ici qu'on voit la puissance de Tailwind : on ajoute l'interaction directement dans les classes.

```html
    <button class="bg-blue-600 text-white p-4 rounded hover:bg-blue-800 transition-colors">
        Acheter
    </button>
```

- `bg-blue-600` : Couleur de base
- `text-white` : Text en blanc
- `p-4` : Padding uniforme tout autour
- `hover:bg-red-500` : **Le bonus !** Quand tu passes la souris, le bleu devient rouge
- `transition-colors` : Petit plus pour que le changement de coumeur soit plus fluide et pas brutal


## Le petit conseil de "pro"

Si tu veux que ton bouton soit plus beau (plus "pro"), on met souvent deux fois plus de padding sur les côtés qu'en haut.

Essaye ça : `px-8 py-3` au lieu de `p-4`. Ça donne un look plus allongé, très moderne !