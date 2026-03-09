```css
/* ============================================================
   EXERCICE 1 : Navigation et États
   ============================================================ */

/* Ciblage de la liste (ul) */
#menu {
    list-style: none; /* Supprime les puces */
    padding: 0;
}

#menu a {
    text-decoration: none; /* Supprime le soulignement */
    color: #333;
    padding: 5px 10px;
}

#menu a.active {
    color: #007bff;
    border-bottom: 2px solid #007bff;
}

#menu a:focus {
    outline: 3px solid orange; 
}

/* ============================================================
   EXERCICE 2 : Positions et Rang (Nth-child)
   ============================================================ */


#cards-container .card:nth-child(1),
#cards-container .card:nth-child(3) {
    border-left: 5px solid blue;
}

#cards-container .card:nth-child(2) {
    border-left: 5px solid orange;
}


#menu li:nth-child(2) a {
    font-weight: bold;
}

/* Réflexion : 
   Si on ajoute un <h2> au début de #cards-container, .card:nth-child(1) ne ciblera PLUS 
   la première carte. Pourquoi ? Parce que :nth-child(1) cherche le PREMIER enfant du 
   parent, quel que soit son type. Le <h2> deviendrait le 1er enfant, et la 
   première carte deviendrait le :nth-child(2).
*/

/* ============================================================
   EXERCICE 3 : Flexbox - Alignement et Menu
   ============================================================ */

#menu {
    display: flex;
    justify-content: center; /* Centre le menu horizontalement */
    gap: 20px; /* espace de 20px entre chaque elements */
}

/* Ton HTML utilise la classe .cta au lieu de .actions */
.cta {
    display: flex;
    gap: 15px;
    justify-content: center; /* Aligne les boutons au centre du Hero */
}

/* ============================================================
   EXERCICE 4 : Grid - La Grille de Cours
   ============================================================ */

#cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); 
    gap: 30px;
}

/* Observation : Avec 2 colonnes (1fr 1fr), la troisième carte passe 
   automatiquement à la ligne suivante (ligne 2, colonne 1) car la grille 
   crée des lignes implicites pour caser le contenu restant.
*/

/* ============================================================
   EXERCICE 5 : Logique et Exclusion
   ============================================================ */


.card:not(.featured) {
    opacity: 0.6;
}


p:empty {
    display: none;
}

/* Signalement visuel pour les champs obligatoires */
input:required {
    border-left: 4px solid red;
}
```