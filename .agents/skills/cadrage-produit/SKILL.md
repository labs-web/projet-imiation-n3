---
name: cadrage-produit
description: >-
  Gouverne le cadrage fonctionnel SMART du MVP (In-Scope / Out-of-Scope) et la justification
  rationnelle approfondie de la stack technique de référence de tout projet web applicatif.
---

# Skill Cadrage Produit : /cadrage-produit

## 1. Mission
Gouverner le cadrage initial, la délimitation fonctionnelle et la faisabilité technologique de tout projet web :
1. Délimiter le périmètre fonctionnel du MVP par la matrice In-Scope vs Out-of-Scope et formaliser les objectifs SMART (`docs/cadrage/note-cadrage.md`).
2. Justifier rationnellement chaque composant de la solution technique de référence (`docs/cadrage/stack-technique.md`).

## 2. Déclenchement
- **Quand l'activer :**
  - Cadrage initial d'un projet web applicatif ou révision de son périmètre.
  - Formalisation des objectifs SMART et de la matrice In-Scope vs Out-of-Scope.
  - Justification technologique et rationnelle des choix d'architecture logicielle.
  - Commande `/cadrage-produit` pour arbitrer le périmètre du MVP ou formaliser la faisabilité technique.
- **Quand NE PAS l'activer :**
  - Immersion usagers et formulation de la vision produit (utiliser `design-thinking-empathie` et `design-thinking-definition`).
  - Architecture détaillée du code et schémas conceptuels (utiliser `architecture-logicielle`).
  - Initialisation de l'espace physique Git (utiliser `init-depot`).

## 3. Missions Disponibles
L'agent identifie le travail demandé et exécute la mission correspondante située dans `missions/` :
- missions/cadrer-perimetre.md : Établit les objectifs SMART, indicateurs KPIs, matrice In-Scope vs Out-of-Scope et contraintes (produit `docs/cadrage/note-cadrage.md`).
- missions/justifier-stack.md : Rédige le dossier de justification rationnelle des composants technologiques (produit `docs/cadrage/stack-technique.md`).

## 4. Règles Obligatoires
- Règle d'unicité : un seul livrable officiel par mission.
- Format Markdown pur sans tableau : listes à puces directes (`- `) exclusives.
- Liens relatifs obligatoires (`./`, `../`).
- Français direct niveau A1/A2 (phrases courtes Sujet + Verbe + Complément).
- Approche générique universelle : applicable à tout projet réel sans dépendance à des tutoriels ou labs.
