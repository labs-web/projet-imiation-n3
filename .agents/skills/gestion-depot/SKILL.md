---
name: gestion-depot
description: >-
  Gère l'initialisation locale Git, la publication sur GitHub via GitHub CLI
  et la structuration conforme du README.md racine selon les standards Solicode.
---

# Skill Gestion de Dépôt : /gestion-depot

## 1. Mission
Piloter l'initialisation et la configuration de base du dépôt du projet, incluant la publication GitHub et la standardisation du fichier `README.md` racine (mission `1.init-projet.mission.md`).

## 2. Déclenchement
- **Quand l'activer** :
  - Exécution de l'étape 1 du flux de travail (`1. Création et initialisation du projet`).
  - Initialisation locale de Git ou publication sur GitHub (`gh repo create`).
  - Nettoyage et structuration du fichier `README.md` racine à partir d'un texte brut.
- **Quand NE PAS l'activer** :
  - Rédaction de documentations pédagogiques ou de labs (utiliser `realisation-ua-lab`).
  - Conception de skills ou règles méta (utiliser `skills-dev`).

## 3. Procédure opératoire pas-à-pas
- **Tâche 1 : Initialisation Git locale** :
  - Vérifier la présence du dépôt Git (`git status`).
  - Si non initialisé : exécuter `git init` et réaliser le commit initial.
- **Tâche 2 : Publication sur GitHub** :
  - Vérifier la connexion avec `gh auth status`.
  - Si non connecté ou `gh` absent : orienter l'apprenant vers le lab `lab-github`.
  - Publier le dépôt via GitHub CLI : `gh repo create`.
- **Tâche 3 : Rédaction et structuration du README.md racine** :
  - Analyser les notes brutes du projet (ex : `READEM.md`).
  - Rédiger le fichier `README.md` racine selon la structure standard ci-dessous.

## 4. Structure standard du README.md racine
- `# [Nom du Projet]`
- `## 1. Description du projet` (résumé en 2-3 phrases, utilisateurs cibles, déploiement)
- `## 2. Contexte et Objectifs` (contexte, objectifs techniques et pédagogiques)
- `## 3. Stack technique` (frontend, backend, base de données, Git)
- `## 4. Organisation des dossiers` (rôle des dossiers : `docs/`, `flux-travail/`, `missions/`, `issues/`, `labs/`, `src/`)
- `## 5. Méthodologie` (Agile/Scrum, 2TUP, Design Thinking)
- `## 6. Démarrage rapide` (prérequis, cloner, lancer)

## 5. Règles obligatoires
- Français A1 et vocabulaire technique professionnel de développeur.
- Aucun tableau Markdown (utiliser exclusivement des listes à puces `- `).
- Liens relatifs exclusifs (`./`, `../`).
