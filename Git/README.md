# Git et GitHub - Guide de Configuration

## Introduction

Mettre un projet sur GitHub permet de sauvegarder son code au fur et à mesure de l'avancée. GitHub fonctionne par un système de versions appelées **commits**.

## Étapes principales

- Avoir un compte GitHub
- Créer un repository GitHub avec GitHubCLI (`gh`)
- Cloner le projet sur son PC
- Coder
- Pousser (`push`) le projet sur GitHub

## 1. Créer un compte GitHub

Créez un compte sur [https://www.github.com](https://www.github.com).

## 2. Installer Git et GitHubCLI

```bash
sudo apt install git
sudo apt install gh
```

### Configurer son identité

```bash
git config --global user.name "Billie JOE"
git config --global user.email joe.billie@gmail.com
```

### Configurer les merges

```bash
git config pull.rebase false
```

## 3. Se connecter à GitHub

```bash
gh auth login
```

## 4. Créer un repository

```bash
git init
gh repo create
```

## 5. Cloner le repository

```bash
git clone https://github.com/VOTRE_NOM/my-repo.git
code my-repo
```

## 6. Publier ses changements

```bash
git add .
git commit -m "Mon message"
git push
```

## 7. Récupérer les changements des collaborateurs

```bash
git pull
```
