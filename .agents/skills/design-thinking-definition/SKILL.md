---
name: design-thinking-definition
description: >-
  Gouverne la phase Définition du Design Thinking : formalisation de la Vision Produit
  (Product Goal), énoncé du Point of View (POV) et cadrage de la proposition de valeur.
---

# Skill Définition & Vision Produit : /design-thinking-definition

## 1. Mission
Prendre en charge la convergence stratégique et la clarification du problème à résoudre pour tout projet web applicatif :
1. Formuler la **Vision Produit (Product Goal)** alignant les parties prenantes et l'équipe de développement.
2. Définir le positionnement, la proposition de valeur unique et les indicateurs stratégiques de succès.
3. Produire le livrable de référence `docs/produit/vision-produit.md`.

## 2. Déclenchement
- **Quand l'activer :**
  - Cadrage stratégique initial ou redéfinition de la vision produit d'une application.
  - Formalisation du Product Goal avant l'établissement du Product Backlog.
  - Commande `/design-thinking-definition` pour formuler ou actualiser la vision produit.
- **Quand NE PAS l'activer :**
  - Immersion terrain et recueil d'empathie utilisateur (utiliser `design-thinking-empathie`).
  - Découpage et estimation des User Stories (utiliser `scrum-product-backlog`).
  - Cadrage du périmètre technique et de la stack (utiliser `cadrage-produit`).

## 3. Missions Disponibles
L'agent identifie le besoin et exécute la mission correspondante située dans `missions/` :
- missions/definir-vision-produit.md : Rédige le document de vision stratégique (`docs/produit/vision-produit.md`) précisant la proposition de valeur, la cible et les métriques de succès.

## 4. Règles Obligatoires
- Démarche 100% générique applicable à tout projet web réel sans dépendance à des tutoriels ou labs.
- Découplage strict entre méthode d'ingénierie et données d'instanciation projet.
- Format Markdown pur sans tableau (listes à puces directes `- ` exclusives).
- Liens relatifs obligatoires (`./`, `../`) et style direct niveau A1/A2.
