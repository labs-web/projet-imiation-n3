---
name: conception-session
description: >-
  Conçoit, découpe et génère les flux de travail par session de formation
  (flux-travail/sessions/) en phases typées (UA-Lab vs UA-Tâche) à partir du flux
  générique d'ingénierie logicielle et des intentions pédagogiques du concepteur.
---

# Skill Conception de Session : /conception-session

## 1. Mission
Générer et actualiser les flux opérationnels de formation (`flux-travail/sessions/flux-travail-s{N}.md`) pour chaque sprint de 80h.
Le skill articule le flux universel d'ingénierie logicielle (25 étapes), les intentions du concepteur (`Sessions/S{N}.md`) et le projet d'imitation (*Blog des Lauréats*).

## 2. Déclenchement
- **Quand l'activer** :
  - Création ou restructuration d'une session de formation (`flux-travail-s{N}.md`).
  - Découpage du projet d'imitation en sprints de formation.
  - Audit de conformité pédagogique d'une session de formation.
- **Quand NE PAS l'activer** :
  - Modification du flux d'ingénierie universel (`flux-travail-generique.md`) -> utiliser `flux-travail`.
  - Rédaction détaillée des tutoriels d'autoformation -> utiliser `realisation-ua-lab`.
  - Cérémonies de fin de sprint -> utiliser `cloture-sprint`.

## 3. Missions disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/generer-session.md : Découpe et génère un flux de session en phases typées (`UA-Lab` vs `UA-Tâche`) selon les règles de gouvernance.
- missions/auditer-session.md : Contrôle la conformité d'une session (typologie des phases, intitulés génériques, zéro tableau, cadre Tri-Projets).

## 4. Typologie Canonique des Phases
- **Phase `UA-Lab`** : Déclenchée lorsqu'un domaine de compétence doit être acquis. Contient obligatoirement :
  1. `Étape : Apprentissage` (notions théoriques et atelier guidé de référence).
  2. `Étape : Application sur le Blog` (mise en pratique immédiate sur le Blog des Lauréats).
- **Phase `UA-Tâche`** : Déclenchée sans nouvel apprentissage conceptuel. Contient exclusivement des tâches d'application opérationnelle (Scrum, Git, Discovery N+1, tests DoD, Review, Rétrospective).
