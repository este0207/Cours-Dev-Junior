```css
/* ============================================================
   EXERCICE 1 : Le "Reset" et la Typographie
   ============================================================ */

body {
    background-color: #f4f4f4;
    font-family: sans-serif;
}

h3 {
    color: navy;
    text-transform: uppercase;
}

.subtitle {
    color: #555;
    font-style: italic;
}

/* ============================================================
   EXERCICE 2 : Maîtriser les Bordures et les États
   ============================================================ */

.card {
    border: 2px solid #ddd;
}

[data-level="beginner"] {
    border: 2px solid #007bff;
    background-color: beige;
}

/* ============================================================
   EXERCICE 3 : Espacement (Margin & Padding)
   ============================================================ */

section {
    padding: 50px 20px; /* Haut/Bas Gauche/Droite */
}

#menu li {
    margin: 20px;
}

.btn.primary {
    padding: 12px 24px;
}

/* ============================================================
   EXERCICE 4 : Relief et Interactivité
   ============================================================ */

.card {
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    border-radius: 10px;
    transition: all 0.3s ease; /* Pour une transition fluide */
}

.card:hover {
    box-shadow: 0 8px 12px rgba(0,0,0,0.2);
    background-color: #d8d8d8; /* Changement léger de fond */
}

button:hover {
    opacity: 0.8;
    cursor: pointer;
}

/* ============================================================
   EXERCICE 5 : Ciblage Chirurgical et Formulaire
   ============================================================ */

#hero h1 {
    font-size: 3rem;
}

input[type="email"]:focus {
    border: 2px solid #007bff;
    outline: none;
}

/* Cible le paragraphe vide dans la dernière carte */
p:empty {
    border: 1px dotted red;
    min-height: 20px; /* Ajouté pour rendre le paragraphe visible même vide */
}
```