# Contexte du Projet

Ce document définit le cadre spécifique du projet pour l'Agent IA.

---

## 1. Identité du projet

- **Nom du projet** : Projet d'imitation - Niveau 3
- **Établissement** : Solicode Tanger
- **Formateur référent** : ESSARRAJ Fouad

---

## 2. Application à réaliser

- **Nom de l'application** : Blog des lauréats
- **Utilisateurs cibles** :
  - Les lauréats : ajout, modification et publication d'articles.
  - Les apprenants de Solicode : consultation et lecture des articles.
- **Déploiement** : L'application sera accessible en ligne sur Internet.

---

## 3. Stack technique et Architecture de l'application

- **Framework Backend** : Laravel 12 (PHP).
- **Architecture logicielle** : Architecture en 2 couches (Contrôleur mince -> Classe Service).
- **Frontend & Vues** : Alpine.js (SPA, composants réactifs), gabarits Blade responsives, HTML5, CSS3, Tailwind CSS.
- **Gestion des erreurs** : Traitement explicite de l'erreur 404 (ressources introuvables).
- **Base de données** : MySQL.
- **Gestion de versions & Outils** : Git, GitHub CLI (`gh`).
- **Intelligence Artificielle & Automatisation** : Agent Antigravity.

---

## 4. Démarche d'ingénierie logicielle

L'apprenant et l'Agent IA appliquent les méthodes suivantes :
- **Méthode par imitation** : Progression par étapes avec tutoriels, labs guidés et veilles technologiques.
- **Processus de développement** : 2TUP et Design Thinking.
- **Modélisation** : Diagramme de contexte et cas d'utilisation modélisés en diagrammes Mermaid.
- **Gestion de projet** : Méthodologie Agile/Scrum (sprints, Product Backlog sous `scrum/`, feuille de route sous `sprints/`).

---

## 5. Identité de l'Agent IA Apprenant
- **Nom officiel :** Agent Réalisation de Sprint (alias `realisation-sprint`)
- **Persona :** Défini dans `.agents/rules/persona.md`. L'agent incarne l'apprenant modèle suivant la formation, réalisant les tutoriels et produisant les livrables du sprint.
- **Normes de Référence Obligatoires :**
  - `.agents/references/gestion-livrables.md` (cartographie et arborescence des livrables)
  - `.agents/references/typologie-uas-tutoriels.md` (catégories d'UAs et slugs des tutoriels)
  - `.agents/references/gitflow.md` (branches sprint[N], commits atomiques et interdiction de commit/push automatique)
- **Souveraineté de l'Apprenant :** L'Agent IA ne committe ni ne pousse jamais de façon autonome. Seul l'apprenant humain effectue les commits et pushs.
