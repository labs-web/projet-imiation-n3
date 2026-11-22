---
name: scrum-sprint-review
description: >-
  Gouverne la conduite de la Sprint Review, la démonstration contradictoire
  de l'incrément devant le Product Owner, l'audit DoD et la décision Go/No-Go.
---

# Skill Sprint Review Scrum : /scrum-sprint-review

## 1. Mission
Prendre en charge la validation contradictoire et l'évaluation de l'incrément de tout sprint Scrum :
1. Animer la démonstration de l'incrément produit face au Product Owner et aux parties prenantes.
2. Auditer la conformité stricte aux critères de la **Definition of Done (DoD)** et aux critères d'acceptation des User Stories.
3. Formaliser la décision officielle **Go / No-Go** d'autorisation du passage au sprint suivant.
4. Produire le procès-verbal officiel de revue `sprints/pv-review-[N].md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Fin d'itération de sprint lors de la cérémonie de Sprint Review.
  - Démonstration contradictoire d'une maquette ou d'un incrément logiciel.
  - Audit d'acceptation des User Stories et arbitrage Go/No-Go.
  - Commande `/scrum-sprint-review` pour auditer ou consigner une revue de sprint.
- **Quand NE PAS l'activer :**
  - Animation du bilan réflexif interne d'équipe (utiliser `scrum-sprint-retrospective`).
  - Planification et contractualisation du sprint (utiliser `scrum-sprint-planning`).
  - Priorisation globale du carnet de produit (utiliser `scrum-product-backlog`).

## 3. Missions Disponibles
L'agent identifie le besoin et exécute la mission correspondante située dans `missions/` :
- missions/conduire-review.md : Rédige le procès-verbal officiel de revue (`sprints/pv-review-[N].md`) incluant démonstration, audit DoD, statut des US et décision Go/No-Go.

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout sprint de projet logiciel réel, sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes hiérarchiques et à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Validation stricte des critères d'acceptation avant d'acter la décision Go.
