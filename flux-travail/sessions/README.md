# Répertoire des Flux de Travail par Session (`flux-travail/sessions/`)

Ce dossier rassemble les flux de travail opérationnels des 9 sessions de formation du niveau N3 (de la session **S0** à la session **S8**).

Chaque session correspond à un sprint de formation de **80 heures** (10 jours). Elle adapte le [Flux de Travail Générique](../flux-travail-generique.md) au contexte pédagogique selon le principe d'apprentissage synchrone : **assimiler une compétence dans une Unité d'Apprentissage d'atelier (UA-Lab) puis l'appliquer immédiatement sur le projet d'imitation**.

---

## 1. Principes d'Organisation d'une Session de Formation

Chaque session articule rigoureusement trois piliers complémentaires :

### Le Cadre Tri-Projets et le Rythme Temporel (80h / 10 jours)
- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas en classe active.
  - Alternance directe entre l'acquisition théorique et la réalisation concrète.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - Épreuve sommative de **Live Coding (40 min chrono sans assistance — 65% de la note)**.
  - Les documents de cadrage et de conception préalable ne sont pas exigés pour le portfolio dans la session.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Développement applicatif métier pur (sans création d'agents IA ni ingénierie de prompt).
  - Clôture de session et bilan réflexif.

### Le Séquençage Direct en Unités d'Apprentissage (UA-Lab vs UA-Tâche)
- **Proscription des Conteneurs « Phases » :** Chaque session est directement découpée selon sa séquence ordonnée d'Unités d'Apprentissage.
- **UA-Lab (Maturité `ua-lab`) :** Ateliers pratiques guidés de formation (guide explicatif Markdown et support de présentation Marp).
- **UA-Tâche (Maturité `projet`) :** Blocs de conduite de projet rattachés obligatoirement à `D.351.2-realisation-projet` (Début, Milieu, Fin).
- **Principe d'antériorité directe :** Chaque UA-Lab est positionné immédiatement avant l'étape de réalisation qui en a besoin.

---

## 2. Table d'Orientation des 9 Sessions N3

- **[Session S0 : Maquette de la Page d'Accueil](./flux-travail-s0.md)**
  - Incrément produit : Maquette interactive de la page d'accueil avec son User Flow textuel, son UI Kit de composants validé, et le cadrage initial du produit (Product Backlog ordonné).
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 5 Unités d'Apprentissage ordonnées (3 UA-Labs et 2 UA-Tâches), 18 étapes.
  - Domaines mobilisés : Scrum (`D.351.1-scrum`), Design Thinking (`D.311.1-design`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S1 : Page de Consultation Publique d'un Article](./flux-travail-s1.md)**
  - Incrément produit : Tranche verticale de consultation d'un article complet sous Laravel 13, modèle Eloquent connecté à MySQL, Service Layer découplé, gabarit Blade responsive Preline UI et gestion robuste 404.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Modélisation UML & Conception Technique (`D.311.2-uml`), Architecture en 2 couches (`D.312.1-architecture`), Laravel 13 & MySQL (`D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S2 : Page d'Accueil Dynamique et Gestion des Catégories](./flux-travail-s2.md)**
  - Incrément produit : Page d'accueil dynamique avec carrousel des derniers articles, filtrage par catégories, CRUD complet des catégories sous architecture MVC + Service et tests d'utilisabilité initiaux.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Design Thinking Empathie (`D.311.1-design`), Modélisation Domaine pur (`D.311.2-uml`), Architecture & Laravel 13 (`D.312.1-architecture` & `D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S3 : Gestion des Articles et Tags Associés (Relations Many-to-Many)](./flux-travail-s3.md)**
  - Incrément produit : Système complet de création et d'édition d'articles avec tags Many-to-Many, validation FormRequest sécurisée, contrôle d'accès par Policies/Gates et formulaire dynamique Preline UI.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Design Thinking POV/HMW (`D.311.1-design`), Modélisation Relations N-N (`D.311.2-uml`), Sécurité Policies/Gates & Eloquent (`D.312.1-architecture` & `D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S4 : Cycle de Vie Éditorial des Articles et Suite de Tests Unitaires](./flux-travail-s4.md)**
  - Incrément produit : Workflow complet de publication des articles (Brouillon, En révision, Publié, Archivé) régi par une machine à états finis, sécurisé par Middlewares HTTP et couvert par une suite de tests unitaires automatisés sous PHPUnit.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Prototypage Preline UI (`D.311.1-design`), Modélisation Machines à états (`D.311.2-uml`), Middlewares & Tests PHPUnit (`D.312.1-architecture` & `D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S5 : Single Page Application Réactive et API REST des Articles](./flux-travail-s5.md)**
  - Incrément produit : Interface Single Page Application réactive avec Alpine.js et Preline UI consommant les endpoints JSON de l'API REST du Blog, validée par un protocole de tests d'utilisabilité par les pairs avec calcul du score SUS.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Tests d'utilisabilité & SUS (`D.311.1-design`), Modélisation DTOs (`D.311.2-uml`), SPA réactive Alpine.js (`D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S6 : Module d'Administration Sécurisé RBAC Développé en TDD](./flux-travail-s6.md)**
  - Incrément produit : Espace d'administration complet du Blog des Lauréats sécurisé par le package Spatie Laravel-Permission (Rôles : Administrateur, Auteur, Lecteur), développé intégralement selon le cycle Red-Green-Refactor de TDD sous PHPUnit.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Matrice RBAC (`D.311.2-uml`), Sécurité Spatie Permission (`D.312.1-architecture`), TDD Red-Green-Refactor (`D.321.1-laravel`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S7 : Application Mobile Android Native Jetpack Compose](./flux-travail-s7.md)**
  - Incrément produit : Application mobile Android native complète en Kotlin avec interface déclarative Jetpack Compose (Scaffold, LazyColumn), architecture MVVM (StateFlow), connectée aux endpoints REST du Blog des Lauréats via Retrofit 2.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 6 Unités d'Apprentissage ordonnées (3 UA-Labs et 3 UA-Tâches), 14 étapes.
  - Domaines mobilisés : Langage Kotlin & Coroutines (`D.323.1-mobile`), Jetpack Compose & Navigation (`D.323.1-mobile`), Consommation d'API REST Retrofit (`D.323.1-mobile`), Réalisation de Projet (`D.351.2-realisation-projet`).

- **[Session S8 : Application Déployée en Production et Binaire Autonome NativePHP](./flux-travail-s8.md)**
  - Incrément produit : Blog des Lauréats packagé et compilé sous forme d'application autonome multiplateforme avec NativePHP, recette globale validée de bout en bout (E2E), déploiement distant en production sans interruption de service et soutenance de certification N3.
  - Durée indicative : 80 heures (10 jours).
  - Organisation : 4 Unités d'Apprentissage ordonnées (2 UA-Labs et 2 UA-Tâches), 8 étapes.
  - Domaines mobilisés : NativePHP multiplateforme (`D.321.1-laravel`), Déploiement en production & DevOps (`D.341.1-devops`), Réalisation de Projet (`D.351.2-realisation-projet`).
