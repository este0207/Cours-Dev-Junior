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



**3. `<img>` - Images**

La balise `<img>` est utilisée pour insérer une image. Contrairement aux balises précédentes, c'est une balise orpheline (ou auto-fermante) : elle n'a pas de balise de fermeture `</img>`.

```html
<img src="chemin/vers/image.jpg" alt="Description de l'image">
```

- `src` (source) : C'est l'attribut le plus important, il indique le chemin (local) ou l'URL (lien internet) de l'image.
- `alt` (alternative) : Ce texte s'affiche si l'image ne peut pas être chargée. Il est crucial pour l'accessibilité (lecteurs d'écran) et le référencement (SEO).

**Exercice 1 :**
- Trouve une image sur le web, fais un clic droit pour "Copier l'adresse de l'image" et colle-la dans l'attribut `src`.
- N'oublie pas de remplir le `alt` avec une description courte.

**Exercice 2 :**
- Ajoute un attribut `width="200"` à ta balise image pour modifier sa largeur manuellement. Que remarques-tu sur la hauteur de l'image ?


**4. `<a>` - Liens**

La balise `<a>...</a>` (pour anchor ou ancre) permet de créer des liens entre les pages. Sans elle, le Web ne serait pas une "toile".

```html
<a href="https://www.google.com">Cliquez ici pour aller sur Google</a>
```

- `href` (hypertext reference) : Indique la destination du lien (l'adresse du site ou d'une autre page de votre projet).
- Le contenu : Le texte placé entre `<a>` et `</a>` devient la zone cliquable (souvent soulignée et bleue par défaut).

**Exercice 1 :**
- Crée un lien qui pointe vers ton réseau social préféré.
- Teste le lien dans ton navigateur pour vérifier qu'il fonctionne.

**Exercice 2 :**
- Ajoute l'attribut `target="_blank"` à l'intérieur de ta balise ouvrante `<a>`.
- Observation : Remarque que le lien s'ouvre maintenant dans un nouvel onglet sans fermer ta page actuelle.
