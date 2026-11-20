# Flux de Travail Opérationnel — Session S02 : Empathie Personas, Architecture MVC + Services & Page d'Accueil

Ce document définit le flux de travail de la **Session S02** (Sprint 2 - 80 heures / 10 jours ouvrés).
Il est structuré en **7 phases typées** alternant les unités d'apprentissage (**UA-Lab**) avec leurs applications immédiates sur le projet d'imitation, et les phases opérationnelles d'ingénierie (**UA-Tâche**).

---

## 1. Fiche d'Identification de la Session S02

- **Identifiant :** Session S02 (Sprint 2)
- **Titre :** Empathie Personas, Architecture MVC + Services & Page d'Accueil Dynamique
- **Durée totale ferme :** 80 heures (10 jours ouvrés)
- **Positionnement :** Deuxième sprint de delivery applicatif Dual-Track
- **Domaines de compétences mobilisés :**
  - Organisation de l'Agent IA en Rules et Skills modulaires (`D.325.1-ia`)
  - Empathie approfondie, Personas et Carte d'Empathie (`D.311.1-design`)
  - Modélisation du Domaine Pur et Diagramme de Classes Mermaid (`D.311.2-uml`)
  - Architecture Logicielle MVC avec Service Layer Multi-Entités (`D.312.1-architecture`)
  - Développement Laravel 13, CRUD Catégories, Preline UI & Page d'Accueil (`D.321.1-laravel`)
- **Objectif global d'apprentissage :**
  - Préparer la branche Git `sprint-2` et actualiser la documentation projet.
  - Organiser l'environnement IA en Rules et Skills modulaires avec **Agent Antigravity & GitHub Copilot**.
  - Conduire l'empathie approfondie du Design Thinking pour lever la dette d'empathie constatée au Sprint 1.
  - Modéliser les classes du domaine pur et les use cases de filtrage en syntaxe Mermaid.
  - Développer sous **Laravel 13** une page d'accueil dynamique complète orchestrée en architecture MVC + Service (Contrôleur `HomeController`, service `ArticleService`, persistance relationnelle MySQL et gabarit Blade sous Preline UI).
  - Préparer la piste Discovery du Sprint 3 et clôturer le sprint par la démonstration et la rétrospective agile.

---

## 2. Organisation dans le Cadre Tri-Projets (80h / 10 jours)

- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas de la page d'accueil dynamique et du CRUD des catégories d'articles.
  - Alternance immédiate : chaque atelier théorique est mis en œuvre sur le Blog.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Codage technique pur en totale autonomie (sans conception ni planification)**.
  - L'apprenant implémente le CRUD compétences et la page d'accueil vitrine de son portfolio sous Laravel 13 et Preline UI.
  - **Épreuve sommative de Live Coding (40 min chrono sans assistance — 65% de la note finale du module)**.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Création du Skill agentique `.agent/skills/category-crud-generator/` pour automatiser la génération d'un CRUD d'entités de classification.
  - Bilan réflexif et consolidation des acquis.

---

## 3. Épreuve de Live Coding (40 min chrono sans assistance — 65% de la note)

- **Contexte :** À partir du projet starter fourni (`dossier-depart/`), implémenter en 40 minutes la page d'accueil du portfolio affichant les 6 réalisations récentes avec leurs étiquettes de catégories sous Preline UI.
- **Consignes opérationnelles :**
  - Déclarer la route d'accueil `/` dans `routes/web.php`.
  - Implémenter le contrôleur mince `HomeController` avec injection de `ArticleService`.
  - Coder la méthode `ArticleService::latestArticles(6)` effectuant la sélection limitée avec tri décroissant.
  - Développer la vue Blade responsive `resources/views/home.blade.php` avec boucle d'affichage et badges de catégories dynamiques Preline UI.
- **Critères d'évaluation :** Séparation stricte MVC + Service, conformité visuelle Preline UI, code propre PSR-12, gestion du cas de liste vide.

---

## 4. Déroulement des 7 Phases de la Session S02

```mermaid
flowchart TD
    subgraph P1 ["Phase 1 : UA-Tâche — Planification & Git"]
        E1["Étape 1 (Application) : Planifier le Sprint N (Sprint Planning S2)"]
        E2["Étape 2 (Application) : Préparer l'environnement de sprint (Branche Git)"]
        E1 --> E2
    end

    subgraph P2 ["Phase 2 : UA-Lab — Rules & Skills IA (D.325.1-ia)"]
        E3["Étape 3 (Apprentissage) : Organisation de l'Agent IA en Rules et Skills"]
        E4["Étape 4 (Application Blog) : Configurer les Rules et Skills du Blog"]
        E3 --> E4
    end

    subgraph P3 ["Phase 3 : UA-Lab — Empathie & Personas (D.311.1-design)"]
        E5["Étape 5 (Apprentissage) : Démarche d'empathie approfondie et carte d'empathie"]
        E6["Étape 6 (Application Blog) : Établir la carte d'empathie et affiner les Personas"]
        E5 --> E6
    end

    subgraph P4 ["Phase 4 : UA-Lab — Classes Domaine Pur Mermaid (D.311.2-uml)"]
        E7["Étape 7 (Apprentissage) : Diagramme de classes du domaine pur en syntaxe Mermaid"]
        E8["Étape 8 (Application Blog) : Modéliser les classes du domaine et les Use Cases"]
        E7 --> E8
    end

    subgraph P5 ["Phase 5 : UA-Lab — Architecture MVC & CRUD Catégories (D.312.1 & D.321.1)"]
        E9["Étape 9 (Apprentissage) : Service Layer multi-entités, filtrage et CRUD Laravel 13"]
        E10["Étape 10 (Application Blog) : Concevoir en détail et développer la tranche"]
        E9 --> E10
    end

    subgraph P6 ["Phase 6 : UA-Tâche — Piste Discovery (Sprint 3)"]
        E11["Étape 11 (Application) : Affiner le Backlog pour le Sprint suivant"]
        E12["Étape 12 (Application) : Modéliser le User Flow et maquetter S3"]
        E11 --> E12
    end

    subgraph P7 ["Phase 7 : UA-Tâche — Qualité, Démonstration & Rétrospective"]
        E13["Étape 13 (Application) : Suivre l'avancement quotidien (Daily Scrum)"]
        E14["Étape 14 (Application) : Tester et valider l'Incrément (DoD)"]
        E15["Étape 15 (Application) : Présenter et inspecter (Sprint Review 2)"]
        E16["Étape 16 (Application) : Améliorer le processus (Sprint Retrospective 2)"]
        E13 --> E14 --> E15 --> E16
    end

    P1 --> P2 --> P3 --> P4 --> P5 --> P6 --> P7
```

---

### Phase 1 : UA-Tâche — Planification du Sprint 2 et Préparation de l'Environnement Git
*Cette phase ne contient pas de nouvel apport théorique. Elle regroupe les tâches opérationnelles d'initialisation du sprint.*

- **Étape 1 (Application) : Planifier le Sprint N (Sprint Planning — Piste Delivery)**
  - Entrées : Product Backlog actualisé, retours de la Review 1 et actions de la Rétrospective S1.
  - Travail d'application sur le Blog : Définir le Sprint Goal S2 ("Déployer la page d'accueil dynamique avec mise en avant des 6 derniers articles et gestion administrable des catégories sous MySQL"), décomposer les User Stories en tâches techniques et valider le Sprint Backlog S2.
  - Sortie (1 seul livrable) : `scrum/sprint-backlog-s2.md`.
- **Étape 2 (Application) : Préparer l'environnement de sprint (Branche Git et README.md)**
  - Entrées : Sprint Backlog S2 validé et branche `main`.
  - Travail d'application sur le Blog : Créer la branche Git `sprint-2`, mettre à jour le fichier `README.md` avec le Sprint Goal S2 et les dates jalons.
  - Sortie (1 seul livrable) : `README.md`.

---

### Phase 2 : UA-Lab — Organisation de l'Agent IA en Rules et Skills Modulaires (Domaine D.325.1-ia)
*Cette phase introduit la structuration modulaire de l'assistance IA dans l'IDE. Elle comprend l'étape d'apprentissage conceptuel suivie de la configuration directe du projet.*

- **Étape 3 (Apprentissage) : Organisation de l'Agent IA en Rules et Skills modulaires**
  - Entrées : Spécifications de l'Agent Antigravity et de GitHub Copilot.
  - Notions de base à apprendre :
    - Découpage modulaire : Rules permanentes (`.agents/rules/`) vs Skills spécialisés (`.agents/skills/`).
    - Format canonique compact des skills ($\le 75$ lignes) et structure des dossiers `missions/`.
    - Context injection et protocoles de déclenchement d'outils.
  - Sortie de l'atelier d'apprentissage (1 seul livrable) : `tutoriels/ia/guide-rules-skills.md`.
- **Étape 4 (Application sur le Blog) : Configurer les Rules et Skills du Blog**
  - Entrées : Guide Rules & Skills et conventions d'architecture du Blog.
  - Travail d'application sur le Blog : Créer et tester les règles de développement spécifiques au Blog des Lauréats pour guider l'agent lors des développements futurs.
  - Sortie (1 seul livrable) : `docs/ia/rules-blog.md`.

---

### Phase 3 : UA-Lab — Empathie Approfondie, Personas et Carte d'Empathie (Domaine D.311.1-design)
*Cette phase introduit l'approfondissement empathique pour corriger la dette méthodologique du Sprint 1. Elle s'organise en une étape d'apprentissage suivie de son application immédiate sur le Blog.*

- **Étape 5 (Apprentissage) : Démarche d'empathie approfondie et carte d'empathie**
  - Entrées : Cadre de Design Thinking.
  - Notions de base à apprendre :
    - Techniques d'entretiens qualitatifs utilisateurs et observation non biaisée.
    - Carte d'empathie à 4 quadrants (Ce qu'il Dit, Fait, Pense, Ressent).
    - Identification des frustrations critiques et des leviers de satisfaction.
  - Sortie de l'atelier d'apprentissage (1 seul livrable) : `tutoriels/design/guide-empathie-personas.md`.
- **Étape 6 (Application sur le Blog) : Établir la carte d'empathie et affiner les Personas du Blog**
  - Entrées : Retours utilisateurs de la Review 1 et guide d'empathie.
  - Travail d'application sur le Blog : Réaliser les cartes d'empathie des profils Lauréat et Lecteur, et actualiser les fiches Personas avec des scénarios d'usage sur la page d'accueil.
  - Sortie (1 seul livrable) : `docs/analyse/carte-empathie-s2.md`.

---

### Phase 4 : UA-Lab — Modélisation du Domaine Pur et Diagramme de Classes Mermaid (Domaine D.311.2-uml)
*Cette phase introduit la modélisation formelle du domaine pur. Elle s'organise en une étape d'apprentissage théorique suivie de la modélisation du domaine du Blog.*

- **Étape 7 (Apprentissage) : Diagramme de classes du domaine pur en syntaxe Mermaid**
  - Entrées : Guide de syntaxe déclarative Mermaid.js.
  - Notions de base à apprendre :
    - Différence fondamentale entre modèle de données relationnel (tables) et diagramme de classes du domaine (entités pures, encapsulation, méthodes).
    - Associations simples, multiplicités (`1..*`, `0..1`), agrégations et compositions.
    - Syntaxe Mermaid `classDiagram` : attributs typés, visibilité (`+`, `-`, `#`) et relations.
  - Sortie de l'atelier d'apprentissage (1 seul livrable) : `tutoriels/uml/guide-classes-domaine.md`.
- **Étape 8 (Application sur le Blog) : Modéliser les classes du domaine et les Use Cases de filtrage**
  - Entrées : Guide Mermaid et vision produit actualisée.
  - Travail d'application sur le Blog : Modéliser le diagramme de classes du domaine pour les entités `Article`, `Category`, `User`, et formaliser les Use Cases de recherche et de filtrage.
  - Sortie (1 seul livrable) : `docs/analyse/classes-domaine-blog.mmd`.

---

### Phase 5 : UA-Lab — Architecture MVC & CRUD Catégories (Domaines D.312.1-architecture & D.321.1-laravel)
*Cette phase introduit le développement multi-entités sous Laravel 13. Elle s'organise en une étape d'apprentissage technique suivie de la réalisation complète sur le Blog, le portfolio et le projet fil rouge.*

- **Étape 9 (Apprentissage) : Service Layer multi-entités, filtrage et CRUD sous Laravel 13 & Preline UI**
  - Entrées : Documentation Laravel 13 et Preline UI.
  - Notions de base à apprendre :
    - Organisation d'une couche Service orchestrant plusieurs entités (`ArticleService` et `CategoryService`).
    - Requêtes Eloquent avec contraintes de sélection, tri (`orderByDesc`), limitations (`take(6)`) et pagination.
    - Élaboration d'un CRUD complet (Create, Read, Update, Delete) avec contrôleur dédié, FormRequest de validation et composants Preline UI.
  - Sortie de l'atelier d'apprentissage (1 seul livrable) : `tutoriels/laravel/guide-home-categories.md`.
- **Étape 10 (Application sur le Blog) : Concevoir en détail et développer (Piste Delivery)**
  - Entrées : Compétences acquises, classes du domaine et maquettes S2.
  - Travail d'application sur le Blog :
    - *Projet d'Imitation :* Coder le contrôleur `HomeController`, le contrôleur `CategoryController`, le service métier étendu, les migrations MySQL des catégories, et la vue d'accueil responsive sous Preline UI avec affichage dynamique des 6 derniers articles.
    - *Projet Technique (Codage pur - Jour 8) :* Coder le CRUD compétences et la page d'accueil de son portfolio personnel (Épreuve de Live Coding de 40 min).
    - *Projet Fil Rouge (Jours 9-10) :* Créer le Skill `.agent/skills/category-crud-generator/` pour automatiser la génération d'un CRUD de taxonomie.
  - Sortie (1 seul livrable) : `app/Http/Controllers/HomeController.php`.

---

### Phase 6 : UA-Tâche — Piste Discovery : Affinement du Backlog et Maquettage du Sprint 3
*Cette phase ne requiert aucun nouvel apport conceptuel. Il s'agit d'une UA-Tâche d'ingénierie opérationnelle pour préparer le sprint suivant.*

- **Étape 11 (Application) : Affiner le Backlog pour le Sprint suivant (Piste Discovery)**
  - Entrées : Product Backlog et retours d'utilisation.
  - Travail d'application : Collaborer avec le Product Owner pour clarifier les User Stories du Sprint 3 (Création sécurisée d'articles, validation de formulaires et tags Many-to-Many).
  - Sortie (1 seul livrable) : `scrum/backlog-refinement-s3.md`.
- **Étape 12 (Application) : Modéliser le User Flow et maquetter pour le Sprint suivant (Piste Discovery)**
  - Entrées : User Stories raffinées pour S3 et UI Kit Preline UI.
  - Travail d'application : Modéliser le flux utilisateur de publication d'article et prototyper les maquettes interactives S3.
  - Sortie (1 seul livrable) : `docs/design/maquettes-sprint-3.md`.

---

### Phase 7 : UA-Tâche — Clôture du Sprint 2, Démonstration, Tests DoD et Rétrospective
*Cette phase opérationnelle rassemble les rituels de clôture et l'analyse réflexive du sprint.*

- **Étape 13 (Application) : Suivre l'avancement quotidien (Daily Scrum — Delivery & Discovery)**
  - Entrées : Tableau Kanban du Sprint 2.
  - Travail d'application : Animer la réunion debout quotidienne de 15 minutes et lever les blocages.
  - Sortie (1 seul livrable) : `issues/issues-sprint-2.md`.
- **Étape 14 (Application) : Tester et valider l'Incrément (Piste Delivery — DoD)**
  - Entrées : Code source du Blog et checklist des 7 critères de la DoD.
  - Travail d'application : Exécuter la checklist de validation (CRUD catégories opérationnel, page d'accueil responsive sous Preline UI, zéro régression).
  - Sortie (1 seul livrable) : `docs/qualite/rapport-dod-sprint-2.md`.
- **Étape 15 (Application) : Présenter et inspecter (Sprint Review N — Double Validation Delivery & Discovery)**
  - Entrées : Incrément logiciel S2 et maquettes du Sprint 3.
  - Travail d'application : Démontrer l'Incrément 2 devant le Product Owner (Groupe 1), valider la page d'accueil et faire tester les maquettes de S3.
  - Sortie (1 seul livrable) : `sprints/pv-review-2.md`.
- **Étape 16 (Application) : Améliorer le processus (Sprint Retrospective N — Amélioration continue)**
  - Entrées : Déroulement de la Review 2 et vécu d'équipe.
  - Travail d'application : Conduire l'analyse réflexive, constater l'efficacité de la levée de la dette d'empathie, et formaliser 2 axes d'amélioration pour S3.
  - Sortie (1 seul livrable) : `scrum/retrospective-s2.md`.
