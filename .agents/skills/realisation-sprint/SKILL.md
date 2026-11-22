---
name: realisation-sprint
description: >-
  Orchestrateur de réalisation opérationnelle d'un sprint étape par étape par jalon.
  Convoque obligatoirement skills-planer avant chaque étape pour créer et faire valider
  la compétence requise, puis exécute l'étape après validation du concepteur.
---

# Skill Réalisation de Sprint : /realisation-sprint

## 1. Mission
Piloter la réalisation opérationnelle des livrables d'un sprint sur le projet d'imitation (*Blog des Lauréats*), structurée en jalons d'ingénierie cohérents.
Pour chaque étape et chaque jalon :
1. **Planification de Jalon :** Cadrer le jalon sous artéfact interactif (`plan-jalon-*.md`).
2. **Protocole de Compétence Pré-Étape :** Convoquer obligatoirement `skills-planer` pour créer la compétence manquante, la soumettre à validation, puis exécuter l'étape.
3. **Bilan de Jalon :** Formaliser la revue finale avant bascule au jalon suivant.

## 2. Déclenchement
- **Quand l'activer :**
  - Lancement ou reprise de l'exécution d'une session de sprint (`flux-travail/sessions/flux-travail-s{N}.md`).
  - Planification du jalon actif d'un sprint (`/realisation-sprint planifier`).
  - Exécution séquentielle des étapes d'un jalon validé (`/realisation-sprint executer`).
  - Validation et bilan de fin de jalon (`/realisation-sprint valider`).
- **Quand NE PAS l'activer :**
  - Rédaction des ateliers d'autoformation didactiques `UA-Lab` (sur Jekyll sous `ua-lab/`).
  - Conception ou arbitrage d'architecture des compétences (utiliser `skills-planer`).
  - Découpage macro pédagogique d'une session (utiliser `conception-session`).

## 3. Missions Disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/planifier-jalon.md : Lit la session active, découpe en jalons homogènes et génère l'artéfact interactif de cadrage du jalon (`plan-jalon-[id].md` avec `RequestFeedback: true`).
- missions/executer-etape.md : Applique le protocole obligatoire en 4 temps : convoquer `skills-planer`, créer le skill, soumettre à validation, puis exécuter l'étape.
- missions/valider-jalon.md : Établit le bilan de complétude des livrables du jalon et sollicite la validation formelle du concepteur avant d'autoriser le jalon suivant.

## 4. Règles Obligatoires
- Protocole Obligatoire Pré-Étape : à chaque étape de flux, convoquer obligatoirement `skills-planer` pour créer le skill/mission manquant, le soumettre à validation du concepteur via artéfact interactif, puis exécuter l'étape uniquement après approbation.
- Découpage obligatoire en jalons : aucune exécution en tunnel sans validation par jalon.
- Règle d'unicité : chaque étape produit un seul livrable principal unique.
- Conformité de style : français direct niveau A1/A2, liens relatifs obligatoires, zéro tableau Markdown.
- Souveraineté Git : interdiction formelle de commit ou de push autonome par l'IA.
