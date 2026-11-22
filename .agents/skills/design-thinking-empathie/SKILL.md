---
name: design-thinking-empathie
description: >-
  Gouverne la phase Empathie du Design Thinking : immersion usagers, formalisation
  de la Carte d'Empathie (4 quadrants) et modélisation des fiches Personas types.
---

# Skill Empathie & Personas : /design-thinking-empathie

## 1. Mission
Prendre en charge l'exploration et la compréhension approfondie des utilisateurs cibles de tout projet web :
1. Structurer l'immersion terrain et synthétiser les observations sous forme de **Carte d'Empathie** (`docs/analyse/empathie.md`).
2. Modéliser les profils archétypaux représentatifs sous forme de **Fiches Personas** (`docs/analyse/personas.md`).

## 2. Déclenchement
- **Quand l'activer :**
  - Phase d'immersion utilisateur et recueil des besoins terrain.
  - Élaboration ou actualisation de la Carte d'Empathie.
  - Modélisation des fiches Personas utilisateurs.
  - Commande `/design-thinking-empathie` pour auditer ou produire les livrables d'empathie.
- **Quand NE PAS l'activer :**
  - Formulation de la vision stratégique globale (utiliser `design-thinking-definition`).
  - Priorisation et rédaction des User Stories (utiliser `scrum-product-backlog`).
  - Prototypage visuel et maquettage d'interface (utiliser `design-thinking-prototypage`).

## 3. Missions Disponibles
L'agent identifie le travail demandé et exécute la mission correspondante située dans `missions/` :
- missions/formaliser-empathie.md : Établit la Carte d'Empathie à 4 quadrants (Dit, Fait, Pense, Ressent) avec analyse des douleurs et gains (`docs/analyse/empathie.md`).
- missions/modeliser-personas.md : Conçoit les fiches Personas détaillées décrivant objectifs, frustrations et opportunités (`docs/analyse/personas.md`).

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout projet web réel sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Unicité des livrables : un seul livrable officiel produit par mission.
