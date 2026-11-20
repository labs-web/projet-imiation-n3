---
name: skills-dev
description: >-
  Gouverne, conçoit, crée et raffine les skills, missions et règles du workspace.
  En appel sans consigne, audite les remarques du concepteur non supportées par défaut
  et propose un plan d'évolution sous forme d'artefact.
---

# Skill Méta-Gouvernance : /skills-dev

## 1. Mission
Gouverner, concevoir, créer et auditer les **Skills** (`.agents/skills/`), leurs **Missions** (`<skill>/missions/<nom>.md`) et les **Règles permanentes** (`.agents/rules/`).
- **Invocation sans argument** : Auditer la discussion, extraire les remarques du concepteur non encore supportées et proposer un plan d'évolution (`plan.md` avec `RequestFeedback: true`).
- **Invocation avec consigne ou étape** : Analyser le besoin ou l'étape du flux (`flux-travail.md`), et arbitrer entre créer un nouveau skill ou ajouter une mission dans un skill existant.

## 2. Déclenchement
- **Quand l'activer** :
  - Audit réflexif des remarques du concepteur (sans argument).
  - Création, mise à jour ou refactorisation d'un skill ou d'une mission.
  - Arbitrage entre règle transverse (`.agents/rules/`) et compétence ciblée (`.agents/skills/`).
- **Quand NE PAS l'activer** :
  - Exécution directe d'une tâche de développement applicatif (utiliser le skill métier dédié).

## 3. Structure canonique obligatoire d'un `SKILL.md`
Tout fichier `SKILL.md` doit respecter strictement ce modèle compact (<= 75 lignes) sans redondance :
- **Frontmatter YAML** : `name` et `description`.
- `## 1. Mission` : Mission générale et périmètre en 1 à 2 phrases directes.
- `## 2. Déclenchement` :
  - **Quand l'activer** : Basé sur le travail demandé par le concepteur (le concepteur formule un besoin métier et ignore les noms internes des missions) ou l'étape du flux.
  - **Quand NE PAS l'activer** : Frontières claires et renvoi vers les skills appropriés.
- `## 3. Missions disponibles` :
  - Formule standard : *« L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` : »*
  - Liste : `- missions/<nom>.md : [Description du travail pris en charge]`.
- **Interdictions formelles** :
  - Aucun protocole abstrait de choix dynamique ou d'étapes de chargement.
  - Aucune répétition des règles transversales (déjà dans `.agents/rules/`).

## 4. Procédure d'intervention
- **Parcours A (Sans consigne)** : Extraire les remarques du concepteur -> Diagnostiquer les écarts -> Émettre un plan d'action sous artefact interactif -> Attendre validation -> Appliquer.
- **Parcours B (Avec consigne / étape)** : Analyser le besoin -> Choisir entre nouvelle mission (`<skill>/missions/<nom>.md`) ou nouveau skill (`.agents/skills/<skill>/SKILL.md`) -> Rédiger selon la structure canonique (<= 75 lignes).
- **Parcours C (Révision réactive d'artéfacts)** : Pour toute révision interactive couplant modification de fichiers de flux et adaptation de skills selon les remarques du concepteur, déléguer au skill `/fixe-plan-and-skills`.
