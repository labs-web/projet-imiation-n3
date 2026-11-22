---
name: scrum-sprint-retrospective
description: >-
  Gouverne l'animation de la Rétrospective agile d'équipe, l'analyse réflexive
  du fonctionnement interne et le plan d'actions d'amélioration continue.
---

# Skill Rétrospective de Sprint : /scrum-sprint-retrospective

## 1. Mission
Prendre en charge l'amélioration continue et l'analyse réflexive de l'équipe de tout projet logiciel :
1. Faciliter l'inspection du fonctionnement d'équipe (relations humaines, processus, outils).
2. Identifier ce qui a bien fonctionné, les irritants, les difficultés et les apprentissages clés.
3. Formaliser un plan d'actions d'amélioration continue composé de 2 à 3 engagements concrets pour le sprint suivant.
4. Produire le livrable officiel `sprints/retrospective-[N].md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Cérémonie de Rétrospective à l'issue de la Sprint Review.
  - Bilan d'amélioration continue de fin d'itération.
  - Commande `/scrum-sprint-retrospective` pour formaliser ou auditer une rétrospective.
- **Quand NE PAS l'activer :**
  - Démonstration produit devant le Product Owner (utiliser `scrum-sprint-review`).
  - Planification du sprint suivant (utiliser `scrum-sprint-planning`).
  - Suivi des cérémonies quotidiennes (utiliser `realisation-sprint`).

## 3. Missions Disponibles
L'agent identifie le besoin et exécute la mission correspondante située dans `missions/` :
- missions/animer-retrospective.md : Rédige le document de rétrospective d'équipe (`sprints/retrospective-[N].md`) incluant analyse réflexive et plan d'engagements.

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout sprint de projet logiciel réel, sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes hiérarchiques et à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Plan d'actions pragmatique limité à 2 ou 3 engagements vérifiables au sprint suivant.
