---
name: scrum-sprint-planning
description: >-
  Gouverne la planification de sprint Scrum, la formulation du Sprint Goal,
  la sélection des User Stories du backlog et le découpage en tâches techniques.
---

# Skill Planification de Sprint : /scrum-sprint-planning

## 1. Mission
Prendre en charge la contractualisation et la préparation opérationnelle de tout sprint Scrum :
1. Définir le **Sprint Goal** unifié aligné sur la valeur incrémentale à délivrer.
2. Sélectionner les User Stories prioritaires du Product Backlog selon la vélocité nominale de l'équipe.
3. Découper les fonctionnalités en tâches techniques d'ingénierie maîtrisables ($\le 8$ heures).
4. Produire le livrable officiel d'engagement d'équipe `sprints/sprint-[N].md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Cérémonie de Sprint Planning en début d'itération.
  - Découpage technique et estimation des tâches d'ingénierie d'un sprint.
  - Formalisation de la feuille d'engagement d'équipe (`sprint-[N].md`).
  - Commande `/scrum-sprint-planning` pour auditer ou lancer la planification d'un sprint.
- **Quand NE PAS l'activer :**
  - Cadrage et priorisation globale du carnet de produit (utiliser `scrum-product-backlog`).
  - Revue contradictoire et rétrospective de clôture de sprint (utiliser `realisation-sprint`).
  - Développement applicatif direct de fonctionnalités (utiliser `developpement-laravel`).

## 3. Missions Disponibles
L'agent identifie le besoin et exécute la mission correspondante située dans `missions/` :
- missions/planifier-sprint.md : Rédige la feuille d'engagement complète du sprint (`sprints/sprint-[N].md`) incluant Sprint Goal, sélection d'US, tâches techniques et DoD.

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout sprint de projet logiciel réel, sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes hiérarchiques et à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Découpage technique granulaire avec une charge unitaire maximale de 8 heures par tâche.
