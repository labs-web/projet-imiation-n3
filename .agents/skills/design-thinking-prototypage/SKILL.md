---
name: design-thinking-prototypage
description: >-
  Gouverne la phase Prototypage du Design Thinking : User Flow textuel,
  spécification d'UI Kit (Tailwind / Preline) et maquettes interactives responsives.
---

# Skill Prototypage & UI Design : /design-thinking-prototypage

## 1. Mission
Prendre en charge la concrétisation visuelle et interactive de tout projet web applicatif :
1. Modéliser les parcours utilisateurs sous forme de **User Flow textuel et arborescent** (`docs/conception/user-flow.md`).
2. Spécifier le Design System modulaire et l'**UI Kit de composants** (`docs/conception/ui-kit.md`).
3. Prototyper les **maquettes interactives et responsives** des écrans clés (`docs/conception/maquettes-sprint-1.md`).

## 2. Déclenchement
- **Quand l'activer :**
  - Modélisation des flux et parcours utilisateurs d'un écran ou d'une fonctionnalité.
  - Conception ou enrichissement de l'UI Kit (palette Tailwind CSS, composants Preline UI).
  - Prototypage de maquettes fonctionnelles et interactives.
  - Commande `/design-thinking-prototypage` pour auditer ou produire les prototypes d'interface.
- **Quand NE PAS l'activer :**
  - Immersion terrain et fiches personas (utiliser `design-thinking-empathie`).
  - Codage applicatif dans l'architecture MVC Laravel (utiliser `developpement-laravel`).
  - Tests d'utilisabilité et validation de recette (utiliser `realisation-sprint`).

## 3. Missions Disponibles
L'agent identifie le besoin et exécute la mission correspondante située dans `missions/` :
- missions/modeliser-user-flow.md : Cartographie les flux utilisateurs arborescents et les scénarios de navigation (`docs/conception/user-flow.md`).
- missions/concevoir-ui-kit.md : Spécifie les tokens de design, la typographie et les composants modulaires (`docs/conception/ui-kit.md`).
- missions/prototyper-maquette.md : Assemble la maquette interactive d'écran avec Tailwind CSS, Preline UI et Alpine.js (`docs/conception/maquettes-sprint-1.md`).

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout projet web réel, sans dépendance à des tutoriels ou labs.
- Zéro tableau Markdown (listes hiérarchiques et à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
- Conception mobile-first, respect des contrastes WCAG AA et utilisation des classes utilitaires officielles.
