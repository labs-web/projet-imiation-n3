---
name: init-depot
description: >-
  Initialise l'infrastructure physique du dépôt Git d'un projet web, configure le .gitignore
  de référence, structure l'arborescence standardisée et rédige le README d'accueil vitrine.
---

# Skill Initialisation du Dépôt : /init-depot

## 1. Mission
Prendre en charge l'initialisation et la mise en conformité de l'espace de développement physique de tout projet web applicatif :
1. Configurer le dépôt Git local et distant avec un `.gitignore` exhaustif adapté à la stack technique retenue (ex: **Laravel 13**, Composer, NPM, IDEs).
2. Structurer et contrôler l'arborescence standardisée des répertoires du projet (`docs/`, `sprints/`, `scrum/`, `src/`).
3. Rédiger la documentation vitrine d'accueil du dépôt (`README.md`) valorisant l'identité, la vision, la stack et le démarrage rapide du projet.

## 2. Déclenchement
- **Quand l'activer :**
  - Initialisation d'un nouveau dépôt Git ou mise en conformité de l'infrastructure d'un projet existant.
  - Réalisation de l'étape de cadrage d'infrastructure et d'accueil du dépôt.
  - Commande `/init-depot` pour initialiser, contrôler ou réaligner l'infrastructure Git et le fichier `README.md`.
- **Quand NE PAS l'activer :**
  - Cadrage fonctionnel ou délimitation du périmètre métier (utiliser `cadrage-produit`).
  - Développement applicatif de fonctionnalités de code (utiliser `developpement-laravel`).
  - Planification des cérémonies et rituels agiles de sprint (utiliser `realisation-sprint`).

## 3. Missions Disponibles
L'agent identifie le travail demandé et exécute la mission correspondante située dans `missions/` :
- missions/initialiser-depot-git.md : Initialise Git, installe le `.gitignore` conforme et structure l'arborescence des répertoires.
- missions/rediger-readme-accueil.md : Rédige le document d'accueil vitrine (`README.md`) valorisant l'identité, la stack, l'organisation et le guide d'installation.

## 4. Règles Obligatoires
- Souveraineté de l'utilisateur : interdiction formelle d'exécuter `git commit` ou `git push` de manière autonome.
- Format Markdown pur sans tableau (listes à puces directes `- ` exclusives).
- Liens relatifs stricts pour tous les chemins documentaires (`./`, `../`).
- Aucune dépendance à des tutoriels ou ateliers pédagogiques : le skill opère sur un projet réel autonome.
