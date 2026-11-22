---
name: scrum-product-backlog
description: >-
  Gouverne la conception, le découpage INVEST, la formulation des critères d'acceptation
  et l'ordonnancement MoSCoW du Product Backlog Scrum de tout projet logiciel.
---

# Skill Product Backlog Scrum : /scrum-product-backlog

## 1. Mission
Prendre en charge la gestion du réservoir vivant des exigences de tout projet web selon le cadre Scrum :
1. Structurer le **Product Backlog** en User Stories complètes et granulaires respectant la norme INVEST.
2. Définir des critères d'acceptation testables pour chaque User Story.
3. Ordonner rigoureusement le backlog selon la méthode de priorisation **MoSCoW** (Must, Should, Could, Won't).
4. Produire le livrable officiel `scrum/product-backlog.md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Initialisation du Product Backlog à partir de la vision produit et des personas.
  - Découpage et estimation de nouvelles User Stories lors des séances d'affinement (Backlog Refinement).
  - Priorisation MoSCoW en préparation d'un sprint planning.
  - Commande `/scrum-product-backlog` pour auditer, enrichir ou réordonner le backlog.
- **Quand NE PAS l'activer :**
  - Cadrage de la vision stratégique globale (utiliser `design-thinking-definition`).
  - Planification détaillée des tâches techniques du sprint actif (utiliser `realisation-sprint`).
  - Développement applicatif des fonctionnalités (utiliser `developpement-laravel`).

## 3. Missions Disponibles
L'agent identifie le travail demandé et exécute la mission correspondante située dans `missions/` :
- missions/ordonner-backlog.md : Établit et ordonne le Product Backlog complet en User Stories INVEST priorisées selon MoSCoW (`scrum/product-backlog.md`).

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout projet web réel sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Respect strict des critères INVEST et formulation canonique des User Stories.
