---
name: gestion-depot
description: >-
  Gère l'initialisation locale Git, la publication sur GitHub via GitHub CLI
  et la structuration conforme du README.md racine selon les standards Solicode.
---

# Skill Gestion de Dépôt : /gestion-depot

## 1. Mission
Piloter l'initialisation et la configuration de base du dépôt du projet, la détection du sprint actif et la standardisation du fichier `README.md` racine (mission encapsulée `missions/init-projet.md`).

## 2. Déclenchement
- **Quand l'activer** :
  - Exécution de l'étape 1 du flux de travail (`1. Création et initialisation du projet`).
  - Initialisation locale de Git, contrôle de branche de sprint ou publication sur GitHub.
  - Nettoyage et structuration du fichier `README.md` racine à partir d'un texte brut.
- **Quand NE PAS l'activer** :
  - Rédaction de labs pédagogiques (utiliser `realisation-ua-lab`).
  - Conception de skills ou règles méta (utiliser `skills-dev`).

## 3. Procédure opératoire pas-à-pas
- **Tâche 1 : Détection Scrum du sprint actif et branche Git** :
  - Vérifier `sprints/sprints.md`. Si absent, le créer avec le Sprint 1 uniquement (ne jamais inventer de futurs sprints).
  - Identifier le sprint ayant le statut **Actif** et sa branche Git associée (`sprint[N]`).
  - Vérifier la branche active (`git branch --show-current`). Si sur `main`, basculer ou créer la branche : `git checkout -b sprint[N]`.
- **Tâche 2 : Initialisation locale Git & Publication GitHub** :
  - Si Git non initialisé : exécuter `git init`.
  - Contrôler `gh auth status`. Si non connecté, orienter vers l'installation et l'authentification de GitHub CLI.
  - Publier le dépôt via GitHub CLI (`gh repo create`) et pousser la branche de sprint (`git push -u origin sprint[N]`).
- **Tâche 3 : Rédaction et structuration du README.md racine** :
  - S'appuyer sur la mission interne `missions/init-projet.md`.
  - Rédiger le fichier `README.md` racine selon le modèle standard ci-dessous.

## 4. Structure standard du README.md racine
- `# [Nom du Projet]`
- `## 1. Description du projet` (résumé en 2-3 phrases, utilisateurs cibles, déploiement)
- `## 2. Contexte et Objectifs` (contexte Solicode, Formateur, méthode par imitation, APC)
- `## 3. Stack technique` (frontend, backend Laravel 12, base de données, Git, IA)
- `## 4. Organisation des dossiers` (`.agents/`, `docs/`, `flux-travail/`, `issues/`, `labs/`, `sprints/`)
- `## 5. Méthodologie` (Agile/Scrum, 2TUP, Design Thinking)
- `## 6. Démarrage rapide` (prérequis, cloner, checkout branche sprint)

## 5. Règles obligatoires
- Français A1 et vocabulaire technique professionnel de développeur.
- Aucun tableau Markdown (utiliser exclusivement des listes à puces `- `).
- Liens relatifs exclusifs (`./`, `../`).
