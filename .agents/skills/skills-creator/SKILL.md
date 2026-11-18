---
name: skills-creator
description: >-
  Gère le cycle de vie des skills de l'Agent IA : création à partir des missions de missions/,
  analyse de la discussion pour proposer de nouveaux skills ou enrichir les skills existants.
  À utiliser quand l'utilisateur demande de créer ou faire évoluer des skills.
---

# Créateur et Évolueur de Skills (`skills-creator`)

Ce skill permet à l'Agent IA de créer, structurer et faire évoluer les skills dans `.agents/skills/`.

## 1. Rôles et déclenchement

- **Cas A : Tâche spécifique demandée par le concepteur** :
  - Créer un nouveau skill dans `.agents/skills/<skill-name>/SKILL.md`.
  - Transformer une ou plusieurs missions de `missions/*.mission.md` en un skill complet.
  - Modifier ou enrichir un skill existant.
- **Cas B : Appel sans travail spécifié (Analyse proactive)** :
  - Analyser l'historique de la discussion et l'état du projet.
  - Identifier les besoins émergents.
  - Proposer dans un artefact plan :
    - Des modifications sur les règles existantes (`.agents/rules/`), ou
    - L'ajout d'une nouvelle mission à un skill existant, ou
    - La création d'un nouveau skill adapté au besoin.

## 2. Structure standard d'un Skill Antigravity

Chaque skill réside dans son propre sous-dossier :
- `.agents/skills/<skill-name>/SKILL.md` (Obligatoire)
- Sous-dossiers optionnels : `scripts/`, `examples/`, `references/`.

### Format du fichier `SKILL.md` :
- **Frontmatter YAML obligatoire** :
  - `name` : Identifiant unique en minuscules avec tirets (`kebab-case`).
  - `description` : Texte à la 3ème personne indiquant **ce que fait le skill** et **quand l'activer**.
- **Corps Markdown** :
  - Instructions étape par étape, claires et compactes.
  - Entrées requises, procédure opératoire et validation.
  - Respect strict des règles générales (Français A1, vocabulaire technique, aucun tableau Markdown, liens relatifs).

## 3. Procédure de création d'un Skill
- Étape 1 : Définir le nom en `kebab-case` et la condition d'activation.
- Étape 2 : Créer le dossier `.agents/skills/<skill-name>/`.
- Étape 3 : Rédiger le fichier `SKILL.md` avec son frontmatter YAML.
- Étape 4 : Vérifier l'absence totale de tableaux Markdown et de liens absolus.
