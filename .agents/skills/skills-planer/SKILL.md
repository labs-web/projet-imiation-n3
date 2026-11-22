---
name: skills-planer
description: >-
  Conçoit et planifie l'écosystème de compétences (Skills et missions).
  Vérifie la couverture de chaque étape de sprint avant sa réalisation,
  critique systématiquement le plan préliminaire pour proposer une meilleure organisation,
  et arbitre entre nouveau skill, ajout de mission ou reconception.
---

# Skill Planification des Compétences : /skills-planer

## 1. Mission
Gouverner la conception et l'adaptation de l'écosystème de compétences (Skills et missions) :
1. **Couverture Pré-Étape & Critique Constructive :** Avant toute réalisation d'une étape de flux de travail lors d'un sprint, s'assurer qu'un skill et une mission existent pour la prendre en charge. Même si un plan préliminaire existe, critiquer systématiquement les prévisions initiales au vu du contexte réel du sprint et proposer une solution supérieure. Arbitrer entre : créer un nouveau skill, ajouter une mission dans un skill existant, ou proposer une reconception de skills.
2. **Plan Préliminaire Guide :** Établir le plan préliminaire global à partir du flux générique (25 étapes), validé par le concepteur et consigné dans `docs/plan-preliminaire-skills.md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Avant de réaliser une étape de sprint, pour valider ou concevoir la compétence qui va l'exécuter (`/skills-planer`).
  - Critique du plan préliminaire et proposition d'une architecture de compétences améliorée.
  - Arbitrage entre nouveau skill, ajout d'une mission dans un skill existant, ou reconception d'architecture.
  - Cadrage préliminaire global de l'écosystème des compétences (`/skills-planer preliminaire`).
- **Quand NE PAS l'activer :**
  - Exécution directe d'une étape de sprint sur le code ou les documents (utiliser `realisation-sprint` une fois le skill en place).
  - Découpage pédagogique des sessions de formation (utiliser `conception-session`).

## 3. Missions Disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/couvrir-etape-sprint.md : Analyse l'étape de sprint à réaliser, critique le plan préliminaire existant, et arbitre sous artéfact interactif entre : nouveau skill, nouvelle mission dans un skill existant, ou reconception de skills.
- missions/planifier-plan-preliminaire.md : Analyse les 25 étapes génériques, émet l'artéfact préliminaire et dépose la boussole validée sous `docs/plan-preliminaire-skills.md`.
- missions/creer-skill.md : Génère l'arborescence physique du skill ou ajoute la mission dans le skill validé (`SKILL.md` $\le 75$ lignes).

## 4. Règles Obligatoires
- Principe de Couverture Préalable : aucune étape de flux de travail n'est exécutée sans skill et mission dédiés confirmés.
- Critique Systématique du Plan Préliminaire : même si `docs/plan-preliminaire-skills.md` existe, ne jamais l'appliquer aveuglément ; le critiquer systématiquement à chaque étape pour proposer une organisation meilleure et plus pertinente.
- Granularité flexible : une mission peut être responsable d'une ou plusieurs étapes de flux de travail selon le découpage retenu.
- Tout arbitrage ou proposition de compétence requiert un artéfact interactif (`RequestFeedback: true`).
- Fichiers `SKILL.md` concis ($\le 75$ lignes), zéro tableau Markdown.
