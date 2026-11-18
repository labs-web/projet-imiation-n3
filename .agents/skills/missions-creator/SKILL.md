---
name: missions-creator
description: >-
  Crée et gère les missions dans missions/*.mission.md et assure la synchronisation
  pédagogique vers les skills de l'Agent IA. À utiliser lors de la création de nouvelles missions d'étapes.
---

# Créateur de Missions et Synchroniseur (`missions-creator`)

Ce skill permet à l'Agent IA de créer des missions dans `missions/` et d'assurer la transition pédagogique vers les skills.

## 1. Rôle et mission pédagogique

- **Création de missions** : Générer des fichiers de missions réutilisables au format `missions/[numéro].[slug].mission.md`.
- **Passerelle de transition vers les Skills** :
  - Assurer la synchronisation entre les missions unitaires du dossier `missions/` et les skills de `.agents/skills/`.
  - Servir de pont pédagogique pendant la phase d'apprentissage : dès que l'apprenant maîtrise la conception directe de skills dans son flux de travail, ce skill de transition ne sera plus requis.

## 2. Structure standard d'une Mission (`*.mission.md`)

Chaque mission générée dans `missions/` doit respecter :
- `# [Titre de la mission] ([numéro].[slug].mission.md)`
- `## Tâches de la mission` (liste ordonnée des tâches à réaliser)
- `## Livrables attendus` (fichiers, dépôts, issues produits)
- `## Protocole d'audit et exécution` :
  - Exécution directe sans plan si l'apprenant spécifie une tâche précise.
  - Audit des livrables et proposition d'un artefact plan si la demande est globale.
- `## Structure du livrable` (template ou plan standard si génération de document)
- `## Règles spécifiques` (Optionnel : uniquement si contraintes techniques particulières propres à l'étape).

## 3. Règles de conception obligatoires
- **Séparation consigne / données** : La mission ne contient jamais le travail à faire en dur ni de placeholder. Le travail est fourni par l'apprenant ou déduit de la conversation.
- **Principe DRY et Héritage** : Ne jamais recopier les règles générales (Français A1, aucun tableau, liens relatifs) déjà formalisées dans `init-ia.mission.md` et `init-agent.mission.md`.
- **Compacité stricte** : Rédiger la mission de façon la plus concise possible, sans texte superflu.
- **Généricité** : 100% générique (applicable à tout projet informatique).
- **Indexation** : Enregistrer obligatoirement la nouvelle mission dans `missions/missions-index.yml`.
