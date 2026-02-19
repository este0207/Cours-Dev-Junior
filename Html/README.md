## 1. Introduction à HTML et CSS

Née en 1989, le **HTML (Hypertext Markup Language) :** est un langage de balisage utilisé pour structurer le contenu des pages web.

**HTML** est le langage déscriptif utilisé pour créer des pages web. Il structure le contenu d'une page en utilisant des balises qui décrivent les éléments à afficher au navigateur.

---

### I. Structure de base

Un fichier commence **TOUJOUR** par cette structure ci :

```html
    <!DOCTYPE html>
    <html lang="fr">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        
    </body>
    </html>
```

- PS: Vous pouvez la génerer automatiquement sur **Vscode** avec `! + entrer` .

---

### II. Analyse des balises 

- `<html lang="fr">...</html>` : Délimite le début et la fin du document .
- `<head>...</head>` : Entête du document , contient les méta-informations `<meta charset="UTF-8">` , le titre de l'onglet (`<title>`), des liens vers des fichiers CSS ou JavaScript, etc... .
- `<body>...</body>` : Corp de notre document, contient toute la partie visible ( text, image, bouton, etc...)

**Exercices 1** : 
- Crée un fichier **HTML** basique avec une structure correcte et ajoute un titre à ta page dans la balise `<h1>` et `<title>`.

---

### III. Les balises principales

**1. `<p>`  paragraphe**
- La balise `<p>...</p>`, est utiliser pour définir un *paragraphe*. Elle englobe du texte et ajoute un espace avant et après le paragraphe.

```html
    <p>Ceci est un paragraphe de texte</p>
```

- Attention à toujours fermer la balise avec une balise `</p>`

**Exercice 1:** 
- Crée trois paragraphes de texte dans le body sans utiliser la balise p. Observe comment les paragraphes ne passent pas à la ligne à chaque paragraphe.

**Exercice 2 :** 
- Ajoute des balises <p> </p> autour de chaque paragraphe de texte et compare la différence avec du texte brut sans balises.

**2. `<h1> - <h6>` - Titres**
- La balise `<h1>...</h1>`, est utiliser pour définir un *Titre*.
```html
    <h1>Grand titre</h1>
    <h2>Sous-titre</h2>
    <h3>Section</h3>
```

- **ATTENTION**: il ne peut y avoir qu'un `h1`par page, il va définir le theme de votre site pour les micro robot du navigateur

**Exercices 1:**
- Crée un titre principal en utilisant la balise `<h1>` et plusieurs sous-titres avec `<h2>` et `<h3>`.

**Exercice 2 :**

- Change l'ordre des balises de titre et regarde comment cela affecte la taille du texte.


**3. `<img>`  paragraphe**

en cour...

**4. `<a>`  paragraphe**

en cour...