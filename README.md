local modification
Modification 13/03/2026 en ligne et encore
# Git - Branches et Fusion

Ce projet est un exercice pratique pour apprendre les bases de Git, notamment la gestion des branches et la fusion de code.

## Concept des branches

Une branche Git permet de travailler sur une version parallèle du projet sans toucher au code principal (`main`). C'est utile pour :

- Développer une nouvelle fonctionnalité sans risquer de casser le projet principal
- Travailler à plusieurs sur des fonctionnalités différentes en même temps
- Tester des idées et les fusionner dans `main` uniquement si elles sont concluantes

## Ce que fait ce tutoriel

Le tutoriel utilise un site web de recettes pour pratiquer Git. Voici les grandes étapes :

### 1. Mise en place
On extrait une archive contenant un site web de recettes, on l'ouvre dans le navigateur et on fait un premier commit pour sauvegarder l'état initial.

### 2. Création d'une branche
On crée une nouvelle branche pour y développer notre recette, sans toucher à `main` :
```bash
git branch ma_branche
git checkout ma_branche
```

### 3. Travail sur la branche
On ajoute sa propre recette en Markdown, on la renomme, on ajoute des images et on édite le HTML pour pointer vers le bon fichier. Chaque étape est committée.

### 4. Visualisation du graphe Git
On peut visualiser l'historique et la structure des branches avec :
```bash
git log --all --graph --decorate
```

### 5. Fusion dans main
Une fois le travail terminé sur la branche, on revient sur `main` et on fusionne :
```bash
git checkout main
git merge ma_branche
```

## Commandes clés utilisées

- `git branch <nom>` — créer une branche
- `git checkout <nom>` — se déplacer sur une branche
- `git mv <source> <destination>` — déplacer/renommer un fichier en gardant l'historique Git
- `git merge <branche>` — fusionner une branche dans la branche courante
- `git log --all --graph --decorate` — visualiser le graphe des commits
