# Mission : Ordonnancement du Product Backlog Scrum (`ordonner-backlog.md`)

## 1. Contexte & Rôle
Cette mission produit le **Product Backlog officiel** de l'application formalisé dans `scrum/product-backlog.md`. Elle fait le pont entre les besoins des personas, la vision produit et la réalisation technique des sprints.

---

## 2. Structure Normative du Product Backlog

Le document est rédigé sans aucun tableau Markdown, en utilisant des listes hiérarchiques claires :

1. **Objectifs & Règles de Gestion du Backlog :**
   - Rappel de la Vision Produit (Product Goal).
   - Règles d'ordonnancement par la valeur métier et l'effort estimé.
   - Norme des User Stories : "En tant que [Persona], je souhaite [Action / Fonctionnalité] afin de [Bénéfice métier]".
   - Critères qualité INVEST : Indépendante, Négociable, apporte de la Valeur, Estimable, Suffisamment petite, Testable.

2. **Épopées Métier (Epics) :**
   - Regroupement des besoins par grands thèmes fonctionnels du projet (ex: Consultation, Publication, Modération, Authentification).

3. **Ordonnancement MoSCoW du Backlog :**
   Pour chaque niveau de priorité :
   - **Must Have (Indispensable pour le MVP) :**
     - Liste détaillée des User Stories prioritaires requises dès la première version.
     - Pour chaque US : identifiant unique (ex: US-01), énoncé standard, critères d'acceptation testables, estimation indicative (Story Points).
   - **Should Have (Important mais contournable temporairement) :**
     - Liste des US à haute valeur ajoutée, planifiées immédiatement après le cœur du MVP.
   - **Could Have (Confort / Valeur ajoutée secondaire) :**
     - Liste des US d'enrichissement ergonomique ou fonctionnel traitées si le temps le permet.
   - **Won't Have (Reporté aux versions ultérieures) :**
     - Fonctionnalités formellement exclues du périmètre du cycle actif pour éviter tout glissement.

4. **Définition de Terminé (Definition of Done - DoD) de Référence :**
   - Critères transverses garantissant la qualité de chaque User Story terminée (code propre, tests validés, responsive vérifié, revue effectuée).
