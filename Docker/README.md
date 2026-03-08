# Bienvenue dans Docker !

Si tu es développeur web, tu as sûrement entendu : **"Mais pourtant, ça marchait sur ma machine !"**

Docker résout ce problème en standardisant les environnements de développement et de production.

## 1. C'est quoi, Docker ?

Docker est une plateforme qui emballe ton application et toutes ses dépendances dans un **conteneur isolé**.

### La métaphore du cargo

Avant les conteneurs maritimes, charger un bateau était complexe. Aujourd'hui, les conteneurs standards simplifient le transport. Docker fait la même chose pour ton code.

## 2. Les 3 concepts clés

| Concept | Définition |
|---------|-----------|
| **Dockerfile** | La recette : instructions pour construire ton environnement |
| **Image** | Le plat cuisiné, figé et prêt à l'emploi |
| **Conteneur** | L'image active et en cours d'exécution |

## 3. Avantages en Dev Web

- **Isolation** : Exécute plusieurs versions (PHP 5.6 et 8.2) sans conflit
- **Cohérence** : Même comportement entre ton PC et production
- **Rapidité** : Configuration en secondes au lieu d'heures

## 4. Commandes essentielles

```bash
docker build -t mon-app .          # Crée une image
docker run -p 8080:80 mon-app      # Lance un conteneur
docker ps                           # Liste les conteneurs actifs
docker stop <id>                    # Arrête un conteneur
```

## 5. Docker Compose

Pour orchestrer plusieurs conteneurs (Frontend, Backend, BDD), utilise `docker-compose up` avec un fichier `docker-compose.yml`.

## En résumé

Docker est une bulle protectrice autour de ton code, garantissant fonctionnement uniforme partout sans polluer ton système.
