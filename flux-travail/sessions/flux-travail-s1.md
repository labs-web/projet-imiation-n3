# Flux de Travail Opérationnel — Session S01 : Consultation Publique d'un Article

Ce document définit le flux de travail de la **Session S01** (Sprint 1) pour le niveau N3.
Il est structuré en **6 phases typées** (3 unités d'apprentissage **UA-Lab** et 3 blocs d'ingénierie opérationnelle **UA-Tâche**), totalisant **14 étapes de travail**.

---

## 1. Fiche d'Identification de la Session S01

- **Identifiant :** Session S01 (Sprint 1)
- **Titre :** Consultation Publique d'un Article (Tranche Verticale découplée MVC + Service)
- **Durée indicative :** 80 heures (10 jours ouvrés) — *fournie à titre indicatif pour le concepteur et les formateurs*
- **Domaines de compétences mobilisés :**
  - Modélisation UML Mermaid (`D.311.2-uml`)
  - Architecture Logicielle en Deux Couches & ADR (`D.312.1-architecture`)
  - Développement Backend Laravel 13, Modèle Eloquent & MySQL, Preline UI & 404 (`D.321.1-laravel`)
- **Objectif global d'apprentissage :**
  - Mettre en place l'environnement de sprint sur Git.
  - Délimiter les frontières système et modéliser les cas d'utilisation en syntaxe déclarative Mermaid.
  - Concevoir une architecture logicielle découplée en 2 couches (Contrôleur mince et Service Layer) formalisée par un Architectural Decision Record (ADR).
  - Développer sous Laravel 13 la consultation d'un article avec modèle Eloquent, base MySQL, composants Preline UI et gestion de l'erreur 404.
  - Préparer la piste Discovery du Sprint 2 et clôturer l'itération avec la détection de la dette d'empathie.

---

## 2. Organisation dans le Cadre Tri-Projets

- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Développement guidé pas-à-pas de la tranche verticale de consultation d'un article.
  - Alternance immédiate : chaque atelier d'apprentissage est appliqué directement sur le code du Blog.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Phase de conception préalable ciblée (1h)** : Élaboration du diagramme de séquence Mermaid de consultation d'une réalisation et formalisation de l'ADR d'architecture (modèle, service, contrôleur).
  - **Épreuve sommative de Live Coding (40 min chrono sans assistance — 65% de la note finale du module)** : Implémentation autonome et fluide de la tranche verticale selon la conception validée (`RealisationController`, `RealisationService`, modèle Eloquent `Realisation` et vue Blade responsive Preline UI).
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Application du découpage architectural et développement de la tranche de consultation d'entité métier avec modèle Eloquent et MySQL sur l'application métier.
  - Bilan réflexif et consolidation des acquis.

---

## 3. Déroulement des 6 Phases de la Session S01

```mermaid
flowchart TD
    subgraph P1 ["Phase 1 : UA-Tâche Début — Planification du Sprint 1 & Préparation Git"]
        E1["Étape 1 : Planifier le Sprint 1"]
        E2["Étape 2 : Préparer l'environnement de sprint (Branche Git & README.md)"]
        E1 --> E2
    end

    subgraph P2 ["Phase 2 : UA-Lab — Modélisation UML Mermaid (D.311.2-uml)"]
        E3["Étape 3 : Tutoriel-lab : Délimiter les frontières système et cas d'utilisation"]
        E4["Étape 4 : Tutoriel-application : Modéliser le contexte et les Use Cases du Blog"]
        E3 --> E4
    end

    subgraph P3 ["Phase 3 : UA-Lab — Architecture MVC + Service (D.312.1-architecture)"]
        E5["Étape 5 : Tutoriel-lab : Structurer le code en architecture découplée et ADR"]
        E6["Étape 6 : Tutoriel-application : Concevoir l'architecture en 2 couches du Blog"]
        E5 --> E6
    end

    subgraph P4 ["Phase 4 : UA-Lab — Modèle Eloquent, Connexion MySQL & Preline UI (D.321.1-laravel)"]
        E7["Étape 7 : Tutoriel-lab : Assimiler modèle Eloquent, MySQL, Preline UI et 404"]
        E8["Étape 8 : Tutoriel-application : Concevoir en détail et développer la consultation"]
        E7 --> E8
    end

    subgraph P5 ["Phase 5 : UA-Tâche Milieu — Piste Discovery (Sprint 2)"]
        E9["Étape 9 : Affiner le Backlog pour le Sprint suivant"]
        E10["Étape 10 : Modéliser le User Flow et les maquettes du Sprint 2"]
        E9 --> E10
    end

    subgraph P6 ["Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité, Démonstration & Rétrospective"]
        E11["Étape 11 : Suivre l'avancement quotidien (Daily Scrum)"]
        E12["Étape 12 : Tester et valider l'Incrément (DoD)"]
        E13["Étape 13 : Présenter et inspecter (Sprint Review 1)"]
        E14["Étape 14 : Améliorer le processus (Sprint Retrospective 1)"]
        E11 --> E12 --> E13 --> E14
    end

    P1 --> P2 --> P3 --> P4 --> P5 --> P6
```

---

### Phase 1 : UA-Tâche Début — Planification du Sprint 1 et Préparation Git
*Cette phase rassemble les tâches opérationnelles d'initialisation de l'itération sans nouvel apport conceptuel.*

- **Étape 1 : Planifier le Sprint 1**
  - Correspondance flux générique : Étape Générique 15 (Planifier le Sprint N).
  - Entrées : Product Backlog initial et capacité d'équipe.
  - Travail d'application sur le Blog : Chaque apprenant endosse le rôle de Product Owner pour son projet (la formation Scrum ayant été assimilée lors du Sprint 0), définit le Sprint Goal S1 ("Permettre aux visiteurs de consulter un article complet connecté à MySQL"), sélectionne la User Story US-01, décompose en tâches de 1 à 4 heures et fixe la Definition of Done.
  - Sortie (1 seul livrable) : `sprints/sprint-1.md`.
- **Étape 2 : Préparer l'environnement de sprint (Branche Git et README.md)**
  - Correspondance flux générique : Étape Générique 16 (Préparer l'environnement de sprint).
  - Entrées : Sprint Backlog S1 validé et branche `main`.
  - Travail d'application sur le Blog : Créer la branche Git `sprint-1`, actualiser le fichier `README.md` avec le Sprint Goal S1, les jalons temporels et la composition d'équipe.
  - Sortie (1 seul livrable) : `README.md`.

---

### Phase 2 : UA-Lab — Modélisation du Contexte et des Cas d'Utilisation en Syntaxe Mermaid (Domaine D.311.2-uml)
*Cette phase introduit la modélisation fonctionnelle déclarative avec alternance immédiate entre apprentissage et application.*

- **Étape 3 : Tutoriel-lab : Délimiter les frontières système et modéliser les cas d'utilisation macro en syntaxe Mermaid**
  - Entrées : Guide de syntaxe déclarative Mermaid.
  - Notions de base à apprendre :
    - Notion de boîte noire système et identification des frontières applicatives.
    - Acteurs externes : primaires et secondaires (Lecteur visiteur, Auteur lauréat, Administrateur).
    - Flux d'échanges entrants et sortants.
    - Cas d'utilisation élémentaires, granularité fonctionnelle, relations d'inclusion (`<<include>>`), extension (`<<extend>>`) et généralisation.
    - Représentation déclarative Mermaid.js (`flowchart` pour le contexte et diagramme des Use Cases macro).
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/uml/cas-utilisation/use-cases-mermaid/use-cases-mermaid.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/uml/cas-utilisation/use-cases-mermaid/presentation-use-cases-mermaid.md`.
- **Étape 4 : Tutoriel-application : Modéliser le contexte et les cas d'utilisation du Blog des Lauréats**
  - Entrées : Guide Mermaid et vision produit du Blog des Lauréats.
  - Travail d'application sur le Blog : Modéliser en syntaxe déclarative Mermaid le diagramme de contexte complet du Blog des Lauréats et formaliser l'ensemble des 15 cas d'utilisation macro du système.
  - Sortie (1 seul livrable) : `docs/analyse/contexte-et-usecases-blog.mmd`.

---

### Phase 3 : UA-Lab — Architecture Logicielle en Deux Couches MVC + Service Layer et Formalisation ADR (Domaine D.312.1-architecture)
*Cette phase introduit le découpage architectural découplé avec alternance immédiate entre apprentissage et application.*

- **Étape 5 : Tutoriel-lab : Structurer le code en architecture découplée MVC + Service et formaliser un ADR**
  - Entrées : Notions de conception logicielle orientée objet.
  - Notions de base à apprendre :
    - Responsabilités respectives du contrôleur mince HTTP (réception, validation de surface, délégation, réponse).
    - Responsabilités de la classe Service métier (règles de gestion, manipulation des données, indépendance du transport HTTP).
    - Principe d'Inversion de Contrôle (IoC) et injection de dépendance automatique par le conteneur Laravel.
    - Structure formelle d'un Architectural Decision Record (ADR) : Titre, Statut, Contexte, Décision, Conséquences.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/architecture/deux-couches/mvc-service/mvc-service.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/architecture/deux-couches/mvc-service/presentation-mvc-service.md`.
- **Étape 6 : Tutoriel-application : Concevoir l'architecture en deux couches de la consultation d'article**
  - Entrées : Cas d'utilisation du Blog et guide d'architecture.
  - Travail d'application sur le Blog : Modéliser le découpage en 2 couches de la tranche de consultation d'un article du Blog et rédiger la décision fondatrice ADR-01 officialisant l'injection de `ArticleService` dans `ArticleController`.
  - Sortie (1 seul livrable) : `docs/architecture/adr-01-consultation-article.md`.

---

### Phase 4 : UA-Lab — Contrôleur Mince, Modèle Eloquent, Connexion MySQL, Preline UI et Gestion Robuste 404 (Domaine D.321.1-laravel)
*Cette phase introduit le développement effectif de la tranche verticale sous Laravel 13 connecté à MySQL avec alternance immédiate entre apprentissage et application.*

- **Étape 7 : Tutoriel-lab : Assimiler le modèle Eloquent, la connexion MySQL, les composants Preline UI et la gestion d'erreur 404**
  - Entrées : Documentation Laravel 13, moteur MySQL et bibliothèque Preline UI.
  - Notions de base à apprendre :
    - Configuration de l'environnement `.env` et connexion à la base de données MySQL.
    - Création de la migration (`create_articles_table`), du Modèle Eloquent `Article` et du Seeder d'initialisation.
    - Déclaration de routes paramétrées dynamiques (`Route::get('/articles/{id}', ...)`) avec contraintes d'identifiant.
    - Injection de dépendance de la classe Service dans le constructeur du contrôleur.
    - Requêtage Eloquent dans la couche Service (`Article::findOrFail($id)` ou levée explicite d'`abort(404)`).
    - Gabarit Blade responsive avec Tailwind CSS et composants de carte Preline UI.
    - Résilience applicative : gestion robuste de l'erreur 404 en cas d'identifiant inexistant.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/laravel/tranche-verticale/show-mysql-preline/show-mysql-preline.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/laravel/tranche-verticale/show-mysql-preline/presentation-show-mysql-preline.md`.
- **Étape 8 : Tutoriel-application : Concevoir en détail et développer la consultation d'un article**
  - Correspondance flux générique : Étape Générique 17 (Concevoir en détail et développer).
  - Entrées : Notions Laravel assimilées, architecture MVC + Service validée, base MySQL configurée et spécifications du Blog.
  - Travail d'application sur le Blog :
    - *Projet d'Imitation :* Coder la migration MySQL, le modèle Eloquent `Article`, le seeder de test, la route `/articles/{id}`, le contrôleur mince `ArticleController`, la classe `ArticleService` requêtant MySQL via Eloquent, la gestion propre de l'erreur 404 (`abort(404)`), et la vue Blade responsive sous Preline UI.
    - *Projet Technique (Jour 8) :* Réaliser la conception préalable (diagramme de séquence Mermaid et ADR express), puis coder la route, le modèle `Realisation`, le contrôleur `RealisationController` et le service `RealisationService` sur son portfolio personnel (Épreuve de Live Coding de 40 min).
    - *Projet Fil Rouge (Jours 9-10) :* Développer la tranche de consultation d'entité métier avec modèle Eloquent et MySQL sur l'application métier.
  - Sortie (1 seul livrable) : `src/app/Services/ArticleService.php`.

---

### Phase 5 : UA-Tâche Milieu — Piste Discovery : Affinement du Backlog et Maquettage du Sprint 2
*Cette phase rassemble les activités d'ingénierie opérationnelle menées en temps masqué (~10% du temps) pour préparer le sprint suivant.*

- **Étape 9 : Affiner le Backlog pour le Sprint suivant**
  - Correspondance flux générique : Étape Générique 18 (Affiner le Backlog pour le Sprint suivant).
  - Entrées : Product Backlog et retours d'utilisation.
  - Travail d'application : Chaque apprenant, dans sa posture de Product Owner, clarifie les User Stories du Sprint 2 (Page d'accueil dynamique et CRUD Catégories avec tables MySQL associées), rédige les critères d'acceptation et estime la complexité en Story Points.
  - Sortie (1 seul livrable) : `scrum/backlog-refinement-s2.md`.
- **Étape 10 : Modéliser le User Flow et les maquettes du Sprint 2**
  - Correspondance flux générique : Étape Générique 19 (Modéliser le User Flow et maquetter pour le Sprint suivant).
  - Entrées : User Stories raffinées pour le Sprint 2 et UI Kit Preline UI.
  - Travail d'application : Modéliser en syntaxe Mermaid le parcours utilisateur de la future page d'accueil et prototyper les maquettes interactives S2 avec les composants Preline UI.
  - Sortie (1 seul livrable) : `docs/conception/maquettes-sprint-2.md`.

---

### Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité DoD, Démonstration et Rétrospective
*Cette phase regroupe les rituels agiles de clôture et la validation de conformité finale du sprint.*

- **Étape 11 : Suivre l'avancement quotidien (Daily Scrum)**
  - Correspondance flux générique : Étape Générique 20 (Suivre l'avancement quotidien).
  - Entrées : Tableau Kanban et tâches du Sprint 1.
  - Travail d'application : Animer la réunion quotidienne debout de 15 minutes, synchroniser les travaux sur le delivery et le discovery, lever immédiatement les points de blocage.
  - Sortie (1 seul livrable) : Mise à jour du suivi des tâches dans `sprints/sprint-1.md`.
- **Étape 12 : Tester et valider l'Incrément (DoD)**
  - Correspondance flux générique : Étape Générique 21 (Tester et valider l'Incrément).
  - Entrées : Code source complet du Blog des Lauréats et critères formels de la Definition of Done.
  - Travail d'application : Exécuter la checklist des 7 critères formels de la DoD (responsive mobile/desktop avec Preline UI, résilience 404 sans régression, respect des standards PSR-12).
  - Sortie (1 seul livrable) : `docs/qualite/rapport-dod-sprint-1.md`.
- **Étape 13 : Présenter et inspecter (Sprint Review 1)**
  - Correspondance flux générique : Étape Générique 22 (Présenter et inspecter).
  - Entrées : Incrément logiciel S1 opérationnel et maquettes interactives du Sprint 2.
  - Travail d'application : Chaque apprenant anime la démonstration de son Incrément 1 en posture de Product Owner, valide la User Story "Consultation d'un article connecté à MySQL", et fait tester les maquettes de S2 aux utilisateurs cibles pour recueillir leurs retours avant le Planning 2.
  - Sortie (1 seul livrable) : `sprints/pv-review-1.md`.
- **Étape 14 : Améliorer le processus (Sprint Retrospective 1)**
  - Correspondance flux générique : Étape Générique 23 (Améliorer le processus).
  - Entrées : Retours de la Review 1 et vécu de l'équipe durant l'itération.
  - Travail d'application : Conduire l'analyse réflexive d'équipe, constater le choc méthodologique de la **dette d'empathie** (avoir développé sans immersion usagers préalable), et décider de prioriser l'immersion Personas dès le début du Sprint 2.
  - Sortie (1 seul livrable) : `sprints/retrospective-1.md`.
