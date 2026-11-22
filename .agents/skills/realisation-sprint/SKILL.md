---
name: realisation-sprint
description: >-
  Orchestrateur de réalisation opérationnelle d'un sprint étape par étape par jalon.
  Vérifie préalablement la couverture de chaque étape par un skill/mission (via skills-planer),
  planifie par jalon avec artéfact interactif, et exécute après validation.
---

# Skill Réalisation de Sprint : /realisation-sprint

## 1. Mission
Piloter la réalisation opérationnelle des livrables d'un sprint sur le projet d'imitation (*Blog des Lauréats*), structurée en jalons d'ingénierie cohérents.
Pour chaque étape et chaque jalon :
1. **Contrôle Préalable de Compétence :** Avant d'exécuter une étape de flux, s'assurer que son skill et sa mission existent ; sinon, déclencher `/skills-planer`.
2. **Cadrage de Jalon :** Planifier et produire un artéfact interactif de cadrage (`plan-jalon-*.md`).
3. **Validation & Exécution :** Demander la validation formelle du concepteur avant exécution pas à pas des livrables.

## 2. Déclenchement
- **Quand l'activer :**
  - Lancement ou reprise de l'exécution d'une session de sprint (`flux-travail/sessions/flux-travail-s{N}.md`).
  - Planification du jalon actif d'un sprint (`/realisation-sprint planifier`).
  - Exécution unitaire d'une étape de sprint couverte par un skill (`/realisation-sprint executer`).
  - Validation et bilan de fin de jalon (`/realisation-sprint valider`).
- **Quand NE PAS l'activer :**
  - Rédaction des ateliers d'autoformation didactiques `UA-Lab` (sur Jekyll sous `ua-lab/`).
  - Conception ou proposition de nouveaux skills ou missions (utiliser `skills-planer`).
  - Découpage macro pédagogique d'une session (utiliser `conception-session`).

## 3. Missions Disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/planifier-jalon.md : Lit la session active, découpe en jalons homogènes et génère l'artéfact interactif de cadrage du jalon (`plan-jalon-[id].md` avec `RequestFeedback: true`).
- missions/executer-etape.md : Vérifie la couverture par un skill/mission dédié (appelle `skills-planer` si absent), puis exécute l'étape et produit son livrable unique.
- missions/valider-jalon.md : Établit le bilan de complétude des livrables du jalon et sollicite la validation formelle du concepteur avant d'autoriser le jalon suivant.

## 4. Règles Obligatoires
- Vérification Préalable Obligatoire : interdiction d'exécuter une étape de flux sans skill et mission dédiés confirmés.
- Découpage obligatoire en jalons : aucune exécution en tunnel sans validation par jalon.
- Règle d'unicité : chaque étape produit un seul livrable principal unique.
- Conformité de style : français direct niveau A1/A2, liens relatifs obligatoires, zéro tableau Markdown.
- Souveraineté Git : interdiction formelle de commit ou de push autonome par l'IA.
