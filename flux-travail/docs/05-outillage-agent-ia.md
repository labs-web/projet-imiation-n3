# Guide d'Accompagnement par l'Agent IA dans le Flux de Travail

Ce document décrit comment l'**Agent IA** intervient comme copilote technique et méthodologique tout au long du flux de travail.

---

## 1. Rôle et Posture de l'Agent IA

L'Agent IA n'est pas un simple générateur de code. Il intervient comme un mentor technique et un garant de la méthode :

- **Perception** : L'agent lit l'arborescence, consulte les règles permanentes (`.agents/rules/`) et audite le travail existant.
- **Décision** : L'agent propose des plans d'implémentation clairs (`/plan`) et attend la validation du concepteur avant d'agir.
- **Action** : L'agent crée ou modifie chirurgicalement les fichiers, exécute des commandes de test et applique les contrôles de conformité.
- **Garde-fous stricts** :
  - L'agent ne commite et ne pousse **jamais** de code sur Git (`git commit` et `git push` restent sous la responsabilité exclusive de l'humain).
  - L'agent ne produit aucun tableau Markdown.
  - L'agent utilise exclusivement des liens relatifs.

---

## 2. Interventions de l'Agent IA par Étape du Flux

### Dans la Phase de Cadrage (Sprint 0) :
- **Aide à la modélisation** : Génération de diagrammes Mermaid (User Flow, cas d'utilisation, classes).
- **Initialisation du socle** : Configuration du dépôt Git, scaffolding Laravel 12 et intégration de Tailwind CSS.
- **Génération documentaire** : Préparation des fiches de cadrage et des fiches Personas.

### Dans les Cycles de Développement (Sprint $N$) :
- **Piste Delivery** :
  - Développement de l'architecture logicielle en 2 couches (Contrôleurs minces vers Classes Services).
  - Rédaction des vues Blade responsives et composants Alpine.js.
  - Mise en place des tests automatisés et vérification de la Definition of Done.
- **Piste Discovery** :
  - Aide à la formalisation des User Stories pour le sprint suivant.
  - Structuration des règles de gestion métier.
- **Fin de sprint** :
  - Support aux cérémonies de clôture via le skill modulaire `cloture-sprint`.
  - Génération des diaporamas de soutenance au format Marp.

### Dans la Synchronisation Inter-Agents (`.sync/`) :
- **Gestion des versions** : Création et incrémentation systématique des fichiers `version.yml` dans l'arborescence miroir `.sync/.../`.
- **Traçabilité** : Mise à jour du front-matter du tutoriel source avec le sprint, le statut de réalisation et la liste des livrables associés avec leurs versions.
