# Répertoire des Flux de Travail par Session (`flux-travail/sessions/`)

Ce dossier rassemble les flux de travail opérationnels des 9 sessions de formation du niveau N3 (de la session **S0** à la session **S8**).

Chaque session correspond à un sprint de formation de **80 heures** (10 jours). Elle adapte le [Flux de Travail Générique](../flux-travail-generique.md) au contexte pédagogique selon le principe d'apprentissage synchrone : **assimiler une compétence dans un UA-lab puis l'appliquer immédiatement sur le projet d'imitation**.

---

## 1. Principes d'Organisation d'une Session de Formation

Chaque session articule rigoureusement trois piliers complémentaires :

### Le Cadre Tri-Projets et le Rythme Temporel (80h / 10 jours)
- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas en classe active.
  - Alternance directe entre l'acquisition théorique et la réalisation concrète.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Développement technique pur en totale autonomie**.
  - L'apprenant réalise uniquement le codage (Laravel 13, Kotlin ou NativePHP) sans phase de planification ni de conception.
  - Épreuve sommative de **Live Coding (40 min chrono sans assistance — 65% de la note)**.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Cinéma)**
  - **Création et enrichissement systématique de Skills agentiques** dans `.agent/skills/`.
  - L'apprenant automatise sur le domaine métier ce qu'il a appris dans le projet d'imitation.
  - Clôture de session et bilan réflexif.

### L'Intercalage Pédagogique des UA-Labs
- **Aucun regroupement en bloc :** Les UA-labs ne sont jamais dispensés à la chaîne en début de sprint.
- **Principe d'antériorité directe :** Chaque UA-lab est positionné immédiatement avant l'étape de réalisation qui en a besoin.
- **Un seul UA-lab par domaine mobilisé :** Toutes les notions d'un même domaine pour la session sont consolidées dans un unique UA-lab.
- **Aucun code hardcodé `UA.*` :** Les unités sont identifiées par leur intitulé et leur domaine (`UA-lab : [Titre] (Domaine D.xxx.x)`). Les codes définitifs seront attribués ultérieurement par l'agent d'autoformation.

### Les Étapes de Réalisation en Noms Génériques
- Toutes les étapes de réalisation reprennent **exclusivement les noms exacts validés du flux générique**.
- Chaque étape de réalisation produit **un seul livrable principal unique**.

---

## 2. Table d'Orientation des 9 Sessions N3

- **[Session S0 : Cadrage, Design Macro & Product Backlog Initial](./flux-travail-s0.md)**
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 5 phases équilibrées (2 phases `UA-Lab` produisant guide explicatif et présentation Marp, et 3 phases `UA-Tâche` d'application opérationnelle : Début, Milieu, Fin).
  - Domaines mobilisés : Scrum (`D.351.1-scrum`), Design Thinking (`D.311.1-design`), UML Mermaid (`D.311.2-uml`).
  - Objectif : Cadrer le projet, initialiser le dépôt Git, organiser l'équipe avec le Groupe 1 (Product Owner), conduire l'immersion usagers et formaliser les Personas, définir la Vision Produit, concevoir la charte graphique avec Preline UI, modéliser le User Flow et les maquettes du Sprint 1 en syntaxe Mermaid, et valider le cadrage lors de la Sprint Review 0 (Jalon Go/No-Go).
  - Correspondance flux générique : Étapes génériques 1 à 11 (14 étapes réparties en 5 phases).

- **[Session S01 : Consultation Publique d'un Article](./flux-travail-s1.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 7 phases typées (4 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : IA & Prompting (`D.325.1-ia`), UML Mermaid (`D.311.2-uml`), Architecture en 2 couches (`D.312.1-architecture`), Laravel 13 (`D.321.1-laravel`).
  - Objectif : Préparer la branche Git `sprint-1`, outiller l'IDE par la méthode RIO, modéliser les frontières et use cases, et coder sous Laravel 13 une tranche verticale de consultation d'article avec service CSV, composants Preline UI et gestion robuste de l'erreur 404.
  - Correspondance flux générique : Étapes génériques 15 à 23 (16 étapes réparties en 7 phases).

- **[Session S02 : Empathie Personas, Architecture MVC + Services & Page d'Accueil](./flux-travail-s2.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 7 phases typées (4 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : IA Rules & Skills (`D.325.1-ia`), Design Thinking Empathie (`D.311.1-design`), UML Domaine pur (`D.311.2-uml`), Architecture Service Layer multi-entités (`D.312.1-architecture`), Laravel 13 & MySQL (`D.321.1-laravel`).
  - Objectif : Lever la dette d'empathie, structurer l'IDE en Rules et Skills, modéliser les classes du domaine pur, développer le CRUD Catégories sous MySQL et la page d'accueil Blade dynamique avec Preline UI.
  - Correspondance flux générique : Étapes génériques 15 à 23 (16 étapes réparties en 7 phases).

- **[Session S03 : Idéation, Définition de Problème, Sécurité (Policies/Gates) & Relations Eloquent](./flux-travail-s3.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 7 phases typées (4 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : Workflows IA (`D.325.1-ia`), Design Thinking POV/HMW (`D.311.1-design`), UML Relations complexes (`D.311.2-uml`), Sécurité Policies/Gates (`D.312.1-architecture`), Laravel 13 FormRequest & Eloquent (`D.321.1-laravel`).
  - Objectif : Formuler le problème métier, modéliser les relations Many-to-Many, sécuriser les formulaires par FormRequest et Policies déclaratives, et manipuler les associations riches Eloquent sous MySQL.
  - Correspondance flux générique : Étapes génériques 15 à 23 (16 étapes réparties en 7 phases).

- **[Session S04 : Prototypage, Tests PHPUnit & Framework Skills](./flux-travail-s4.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 7 phases typées (4 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : Framework de Skills IA (`D.325.1-ia`), Prototypage Preline UI (`D.311.1-design`), UML Machines à états (`D.311.2-uml`), Sécurité Middlewares (`D.312.1-architecture`), Tests automatisés PHPUnit (`D.321.1-laravel`).
  - Objectif : Prototyper les écrans complexes sous Preline UI, modéliser les états finis, intercepter les flux HTTP par middlewares, et automatiser les tests unitaires de service sous PHPUnit.
  - Correspondance flux générique : Étapes génériques 15 à 23 (16 étapes réparties en 7 phases).

- **[Session S05 : Tests Utilisateurs, SPA Alpine.js & Agent IA](./flux-travail-s5.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 7 phases typées (4 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : Agent IA autonome (`D.325.1-ia`), UML DTOs (`D.311.2-uml`), SPA réactive Alpine.js (`D.321.1-laravel`), Tests utilisateurs Peer Testing (`D.311.1-design`).
  - Objectif : Configurer un agent IA en boucle fermée, développer une SPA réactive avec Alpine.js et requêtes asynchrones fetch(), et conduire un protocole rigoureux de Peer Testing avec calcul du score SUS.
  - Correspondance flux générique : Étapes génériques 15 à 23 (16 étapes réparties en 7 phases).

- **[Session S06 : Sécurité Spatie (RBAC) & TDD Complet](./flux-travail-s6.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 6 phases typées (3 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : UML Matrice RBAC (`D.311.2-uml`), Sécurité Spatie Permission (`D.312.1-architecture`), TDD Red-Green-Refactor (`D.321.1-laravel`).
  - Objectif : Modéliser les habilitations, installer le standard Spatie Laravel-Permission sous MySQL, et appliquer la démarche TDD complète sous PHPUnit pour verrouiller les accès avant le code de production.
  - Correspondance flux générique : Étapes génériques 15 à 23 (14 étapes réparties en 6 phases).

- **[Session S07 : Kotlin & Android Studio (Client Mobile)](./flux-travail-s7.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 6 phases typées (3 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 3 phases `UA-Tâche` d'application opérationnelle pure).
  - Domaines mobilisés : Langage Kotlin & Coroutines (`D.323.1-mobile`), Jetpack Compose & Navigation (`D.323.1-mobile`), Consommation d'API REST Retrofit (`D.323.1-mobile`).
  - Objectif : Maîtriser Kotlin et Compose, construire une interface mobile réactive avec LazyColumn et NavHost, et consommer l'API REST Laravel 13 en mobilité.
  - Correspondance flux générique : Étapes génériques 15 à 23 (14 étapes réparties en 6 phases).

- **[Session S08 : Portabilité NativePHP, Recette Globale, Déploiement en Production & Soutenance N3](./flux-travail-s8.md)**
  - Durée : 80 heures (10 jours).
  - Organisation : 4 phases typées (2 phases `UA-Lab` avec alternance immédiate Apprentissage $\to$ Application sur le Blog, et 2 phases `UA-Tâche` de déploiement et soutenance officielle).
  - Domaines mobilisés : NativePHP multiplateforme (`D.321.1-laravel`), Déploiement en production & DevOps (`D.341.1-devops`), Soutenance de qualification N3.
  - Objectif : Packager l'application Laravel sous forme de binaire autonome avec NativePHP, conduire la recette globale et le déploiement en production (Étape 24 du flux générique), et soutenir devant le jury officiel de certification N3 (Étape 25 du flux générique).
  - Correspondance flux générique : Étapes génériques 15 à 25 (8 étapes réparties en 4 phases).

---

## 3. Règles Qualité Communes

- **Zéro tableau Markdown :** Tous les documents utilisent exclusivement des listes à puces directes (`- `).
- **Liens 100% relatifs :** Tous les liens vers le flux générique ou les documents annexes sont portables.
- **Français niveau A1 :** Phrases courtes, actives et directes adaptées aux développeurs en formation.
