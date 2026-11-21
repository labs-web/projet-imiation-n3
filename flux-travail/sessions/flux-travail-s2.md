# Flux de Travail Opérationnel — Session S2 : Page d'Accueil Dynamique et Gestion des Catégories

Ce document définit le flux de travail opérationnel de la **Session S2** (Sprint 2) pour le niveau N3.
Il est centré sur la production de son incrément majeur : la **Page d'Accueil Dynamique et la Gestion des Catégories** du Blog des Lauréats.

Le flux sépare de manière étanche les Unités d'Apprentissage d'ateliers pratiques (**UA-Lab**) et les Unités d'Apprentissage d'application opérationnelle sur le projet (**UA-Tâche**), totalisant **6 UAs** et **14 étapes de travail**.

Les durées temporelles (80 heures / 10 jours) sont fournies à titre purement indicatif pour les formateurs et le concepteur.

---

## 1. Fiche d'Identification de la Session S2

- **Identifiant :** Session S2 (Sprint 2)
- **Titre centré sur l'incrément :** Page d'Accueil Dynamique et Gestion des Catégories
- **Incrément produit :** Page d'accueil dynamique avec carrousel des derniers articles, filtrage par catégories, CRUD complet des catégories sous architecture MVC + Service et tests d'utilisabilité initiaux
- **Durée indicative :** 80 heures (10 jours ouvrés)
- **Positionnement :** Deuxième sprint de delivery applicatif Dual-Track
- **Référentiel des compétences :** Conforme au document de référence [.agents/references/domaines-competences.md](../../.agents/references/domaines-competences.md)
- **Domaines de compétences et Unités d'Apprentissage mobilisés :**
  - Domaine Conception & Design Thinking (`D.311.1-design`) :
    - Unité d'apprentissage (UA-Lab) : *Empathie approfondie et personas du Blog* (Statut : **À réaliser**)
  - Domaine Modélisation UML & Conception Technique (`D.311.2-uml`) :
    - Unité d'apprentissage (UA-Lab) : *Modélisation du domaine pur et diagramme de classes* (Statut : **À réaliser**)
  - Domaine Architecture Logicielle (`D.312.1-architecture`) & Backend Laravel (`D.321.1-laravel`) :
    - Unité d'apprentissage (UA-Lab) : *Architecture MVC multi-services et CRUD Catégories* (Statut : **À réaliser**)
  - Domaine Réalisation et Conduite de Projet (`D.351.2-realisation-projet`) :
    - Unité d'apprentissage 1 (UA-Tâche) : *Planification du Sprint 2 et Préparation Git* (Statut : **À réaliser**)
    - Unité d'apprentissage 2 (UA-Tâche) : *Piste Discovery : Affinement du Backlog et Maquettage du Sprint 3* (Statut : **À réaliser**)
    - Unité d'apprentissage 3 (UA-Tâche) : *Suivi Quotidien, Qualité DoD, Démonstration et Rétrospective* (Statut : **À réaliser**)
- **Objectif global d'apprentissage :**
  - Préparer la branche Git `sprint-2` et actualiser la documentation projet.
  - Conduire l'empathie approfondie du Design Thinking pour lever la dette d'empathie constatée au Sprint 1.
  - Modéliser les classes du domaine pur et les use cases de filtrage en syntaxe déclarative textuelle.
  - Développer sous **Laravel 13** une page d'accueil dynamique complète orchestrée en architecture MVC + Service (Contrôleur `HomeController`, service `ArticleService`, persistance relationnelle MySQL et gabarit Blade sous Preline UI).
  - Préparer la piste Discovery du Sprint 3 et clôturer le sprint par la démonstration et la rétrospective agile.

---

## 2. Organisation dans le Cadre Tri-Projets

- **Rôles Scrum & Autonomie :** Chaque apprenant endosse le rôle de Product Owner pour son propre projet et pilote son backlog en autonomie.
- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas de la page d'accueil dynamique et du CRUD des catégories d'articles.
  - Alternance immédiate : chaque atelier théorique est mis en œuvre sur le Blog.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Épreuve sommative de Live Coding (40 min chrono sans assistance — 65% de la note finale du module)** : Implémentation du CRUD compétences et de la page d'accueil vitrine de son portfolio sous Laravel 13 et Preline UI.
  - **Règle formelle d'exigence :** Les documents de cadrage et de conception préalable ne sont pas demandés pour le portfolio dans la session.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Développement du CRUD de classification d'entités avec modèle Eloquent et persistance MySQL sur l'application fil rouge (développement logiciel métier pur, sans agents IA ni ingénierie de prompt).
  - Bilan réflexif et consolidation des acquis.

---

## 3. Épreuve de Live Coding (40 min chrono sans assistance — 65% de la note)

- **Contexte :** À partir du projet starter fourni (`dossier-depart/`), implémenter en 40 minutes la page d'accueil du portfolio affichant les 6 réalisations récentes avec leurs étiquettes de catégories sous Preline UI.
- **Consignes opérationnelles :**
  - Déclarer la route d'accueil `/` dans `src/routes/web.php`.
  - Implémenter le contrôleur mince `HomeController` avec injection de `ArticleService`.
  - Coder la méthode `ArticleService::latestArticles(6)` effectuant la sélection limitée avec tri décroissant.
  - Développer la vue Blade responsive `src/resources/views/home.blade.php` avec boucle d'affichage et badges de catégories dynamiques Preline UI.
- **Critères d'évaluation :** Séparation stricte MVC + Service, conformité visuelle Preline UI, code propre PSR-12, gestion du cas de liste vide.

---

## 4. Déroulement Opérationnel des 6 Unités d'Apprentissage du Sprint 2

```mermaid
flowchart TD
    subgraph UA1 ["UA-Tâche Début : Planification du Sprint 2 & Préparation Git (D.351.2-realisation-projet)"]
        E1["Étape 1 : Planifier le Sprint 2 (À réaliser)"]
        E2["Étape 2 : Préparer l'environnement de sprint (Branche Git & README.md) (À réaliser)"]
        E1 --> E2
    end

    subgraph UA2 ["UA-Lab : Empathie & Personas (D.311.1-design)"]
        E3["Étape 3 : Tutoriel-lab : Démarche d'empathie approfondie et carte d'empathie (À réaliser)"]
        E4["Étape 4 : Tutoriel-application : Établir la carte d'empathie et affiner les Personas (À réaliser)"]
        E3 --> E4
    end

    subgraph UA3 ["UA-Lab : Modélisation du Domaine Pur et Diagramme de Classes (D.311.2-uml)"]
        E5["Étape 5 : Tutoriel-lab : Diagramme de classes du domaine pur en syntaxe déclarative (À réaliser)"]
        E6["Étape 6 : Tutoriel-application : Modéliser les classes du domaine et les Use Cases (À réaliser)"]
        E5 --> E6
    end

    subgraph UA4 ["UA-Lab : Architecture MVC & CRUD Catégories (D.312.1 & D.321.1)"]
        E7["Étape 7 : Tutoriel-lab : Service Layer multi-entités et CRUD Laravel 13 (À réaliser)"]
        E8["Étape 8 : Tutoriel-application : Concevoir en détail et développer la page d'accueil (À réaliser)"]
        E7 --> E8
    end

    subgraph UA5 ["UA-Tâche Milieu : Piste Discovery du Sprint 3 (D.351.2-realisation-projet)"]
        E9["Étape 9 : Affiner le Backlog pour le Sprint suivant (À réaliser)"]
        E10["Étape 10 : Modéliser le User Flow et les maquettes du Sprint 3 (À réaliser)"]
        E9 --> E10
    end

    subgraph UA6 ["UA-Tâche Fin : Suivi Quotidien, Qualité, Démonstration & Rétrospective (D.351.2-realisation-projet)"]
        E11["Étape 11 : Suivre l'avancement quotidien (Daily Scrum) (À réaliser)"]
        E12["Étape 12 : Tester et valider l'Incrément (DoD) (À réaliser)"]
        E13["Étape 13 : Présenter et inspecter (Sprint Review 2) (À réaliser)"]
        E14["Étape 14 : Améliorer le processus (Sprint Retrospective 2) (À réaliser)"]
        E11 --> E12 --> E13 --> E14
    end

    UA1 --> UA2 --> UA3 --> UA4 --> UA5 --> UA6
```

---

### Unité d'Apprentissage (UA-Tâche) : Planification du Sprint 2 et Préparation Git (Domaine D.351.2-realisation-projet)
*Bloc opérationnel d'initialisation du sprint sans nouvel apport théorique.*

- **Étape 1 : Planifier le Sprint 2**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 15 (Planifier le Sprint N).
  - Entrées : Product Backlog actualisé, retours de la Review 1 et actions de la Rétrospective S1.
  - Travail d'application sur le Blog : Chaque apprenant endosse le rôle de Product Owner pour son projet, définit le Sprint Goal S2 ("Déployer la page d'accueil dynamique avec mise en avant des 6 derniers articles et gestion administrable des catégories sous MySQL"), décompose les User Stories en tâches techniques et valide le Sprint Backlog S2.
  - Sortie (1 seul livrable) : `sprints/sprint-2.md`.
- **Étape 2 : Préparer l'environnement de sprint (Branche Git et README.md)**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 16 (Préparer l'environnement de sprint).
  - Entrées : Sprint Backlog S2 validé et branche `main`.
  - Travail d'application sur le Blog : Créer la branche Git `sprint-2`, mettre à jour le fichier `README.md` avec le Sprint Goal S2 et les dates jalons.
  - Sortie (1 seul livrable) : `README.md`.

---

### Unité d'Apprentissage (UA-Lab) : Empathie Approfondie, Personas et Carte d'Empathie (Domaine D.311.1-design)
*Atelier d'apprentissage pratique de l'approfondissement empathique pour lever la dette méthodologique du Sprint 1.*

- **Étape 3 : Tutoriel-lab : Démarche d'empathie approfondie et carte d'empathie**
  - Statut : **À réaliser**
  - Unité d'apprentissage : *Empathie approfondie et personas du Blog*.
  - Entrées : Cadre de Design Thinking.
  - Notions de base à apprendre :
    - Techniques d'entretiens qualitatifs utilisateurs et observation non biaisée.
    - Carte d'empathie à 4 quadrants (Ce qu'il Dit, Fait, Pense, Ressent).
    - Identification des frustrations critiques et des leviers de satisfaction.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/design/empathie/empathie-approfondie/empathie-approfondie.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/design/empathie/empathie-approfondie/presentation-empathie-approfondie.md`.
- **Étape 4 : Tutoriel-application : Établir la carte d'empathie et affiner les Personas du Blog**
  - Statut : **À réaliser**
  - Unité d'apprentissage : *Empathie approfondie et personas du Blog*.
  - Entrées : Retours utilisateurs de la Review 1 et guide d'empathie.
  - Travail d'application sur le Blog : Réaliser les cartes d'empathie des profils Lauréat et Lecteur, et actualiser les fiches Personas avec des scénarios d'usage sur la page d'accueil.
  - Sortie (1 seul livrable) : `docs/analyse/carte-empathie-s2.md`.

---

### Unité d'Apprentissage (UA-Lab) : Modélisation du Domaine Pur et Diagramme de Classes (Domaine D.311.2-uml)
*Atelier d'apprentissage pratique de la modélisation formelle du domaine pur avec alternance directe.*

- **Étape 5 : Tutoriel-lab : Diagramme de classes du domaine pur en syntaxe déclarative**
  - Statut : **À réaliser**
  - Unité d'apprentissage : *Modélisation du domaine pur et diagramme de classes*.
  - Entrées : Guide de syntaxe déclarative textuelle.
  - Notions de base à apprendre :
    - Différence fondamentale entre modèle de données relationnel (tables) et diagramme de classes du domaine (entités pures, encapsulation, méthodes).
    - Associations simples, multiplicités (`1..*`, `0..1`), agrégations et compositions.
    - Représentation déclarative textuelle : attributs typés, visibilité (`+`, `-`, `#`) et relations.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/uml/classes-domaine/classes-domaine-pur/classes-domaine-pur.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/uml/classes-domaine/classes-domaine-pur/presentation-classes-domaine-pur.md`.
- **Étape 6 : Tutoriel-application : Modéliser les classes du domaine et les Use Cases de filtrage**
  - Statut : **À réaliser**
  - Unité d'apprentissage : *Modélisation du domaine pur et diagramme de classes*.
  - Entrées : Guide de modélisation et vision produit actualisée.
  - Travail d'application sur le Blog : Modéliser le diagramme de classes du domaine pour les entités `Article`, `Category`, `User`, et formaliser les Use Cases de recherche et de filtrage.
  - Sortie (1 seul livrable) : `docs/analyse/classes-domaine-blog.mmd`.

---

### Unité d'Apprentissage (UA-Lab) : Architecture MVC & CRUD Catégories (Domaines D.312.1-architecture & D.321.1-laravel)
*Atelier d'apprentissage pratique du développement multi-entités sous Laravel 13.*

- **Étape 7 : Tutoriel-lab : Service Layer multi-entités, filtrage et CRUD sous Laravel 13 & Preline UI**
  - Statut : **À réaliser**
  - Unité d'apprentissage : *Architecture MVC multi-services et CRUD Catégories*.
  - Entrées : Documentation Laravel 13 et Preline UI.
  - Notions de base à apprendre :
    - Organisation d'une couche Service orchestrant plusieurs entités (`ArticleService` et `CategoryService`).
    - Requêtes Eloquent avec contraintes de sélection, tri (`orderByDesc`), limitations (`take(6)`) et pagination.
    - Élaboration d'un CRUD complet (Create, Read, Update, Delete) avec contrôleur dédié, FormRequest de validation et composants Preline UI.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/laravel/crud-categories/crud-categories-mysql/crud-categories-mysql.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/laravel/crud-categories/crud-categories-mysql/presentation-crud-categories-mysql.md`.
- **Étape 8 : Tutoriel-application : Concevoir en détail et développer la page d'accueil dynamique**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.321.1-laravel`.
  - Correspondance flux générique : Étape Générique 17 (Concevoir en détail et développer).
  - Entrées : Compétences acquises, classes du domaine et maquettes S2.
  - Travail d'application sur le Blog :
    - *Projet d'Imitation :* Coder le contrôleur `HomeController`, le contrôleur `CategoryController`, le service métier étendu, les migrations MySQL des catégories, et la vue d'accueil responsive sous Preline UI avec affichage dynamique des 6 derniers articles.
    - *Projet Technique (Jour 8) :* Coder le CRUD compétences et la page d'accueil de son portfolio personnel (Épreuve de Live Coding de 40 min).
    - *Projet Fil Rouge (Jours 9-10) :* Développer le CRUD de classification d'entités avec modèle Eloquent et MySQL sur l'application fil rouge.
  - Sortie (1 seul livrable) : `src/app/Http/Controllers/HomeController.php`.

---

### Unité d'Apprentissage (UA-Tâche) : Piste Discovery : Affinement du Backlog et Maquettage du Sprint 3 (Domaine D.351.2-realisation-projet)
*Bloc d'ingénierie opérationnelle mené en temps masqué pour préparer le sprint suivant.*

- **Étape 9 : Affiner le Backlog pour le Sprint suivant**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 18 (Affiner le Backlog pour le Sprint suivant).
  - Entrées : Product Backlog et retours d'utilisation.
  - Travail d'application : Chaque apprenant, dans sa posture de Product Owner, clarifie les User Stories du Sprint 3 (Création sécurisée d'articles, validation de formulaires et tags Many-to-Many), rédige les critères d'acceptation et estime la complexité en Story Points.
  - Sortie (1 seul livrable) : `scrum/backlog-refinement-s3.md`.
- **Étape 10 : Modéliser le User Flow et les maquettes du Sprint 3**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 19 (Modéliser le User Flow et maquetter pour le Sprint suivant).
  - Entrées : User Stories raffinées pour S3 et UI Kit Preline UI.
  - Travail d'application : Modéliser le flux utilisateur de publication d'article et prototyper les maquettes interactives S3.
  - Sortie (1 seul livrable) : `docs/conception/maquettes-sprint-3.md`.

---

### Unité d'Apprentissage (UA-Tâche) : Suivi Quotidien, Qualité DoD, Démonstration et Rétrospective (Domaine D.351.2-realisation-projet)
*Rituels agiles de clôture et analyse réflexive du sprint.*

- **Étape 11 : Suivre l'avancement quotidien (Daily Scrum)**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 20 (Suivre l'avancement quotidien).
  - Entrées : Tableau Kanban du Sprint 2.
  - Travail d'application : Animer la réunion debout quotidienne de 15 minutes et lever les blocages.
  - Sortie (1 seul livrable) : Mise à jour du suivi des tâches dans `sprints/sprint-2.md`.
- **Étape 12 : Tester et valider l'Incrément (DoD)**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 21 (Tester et valider l'Incrément).
  - Entrées : Code source du Blog et checklist des 7 critères de la DoD.
  - Travail d'application : Exécuter la checklist de validation (CRUD catégories opérationnel, page d'accueil responsive sous Preline UI, zéro régression).
  - Sortie (1 seul livrable) : `docs/qualite/rapport-dod-sprint-2.md`.
- **Étape 13 : Présenter et inspecter (Sprint Review 2)**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 22 (Présenter et inspecter).
  - Entrées : Incrément logiciel S2 et maquettes du Sprint 3.
  - Travail d'application : Chaque apprenant anime la démonstration de son Incrément 2 en posture de Product Owner, valide la page d'accueil et fait tester les maquettes de S3.
  - Sortie (1 seul livrable) : `sprints/pv-review-2.md`.
- **Étape 14 : Améliorer le processus (Sprint Retrospective 2)**
  - Statut : **À réaliser**
  - Domaine de compétence : `D.351.2-realisation-projet`.
  - Correspondance flux générique : Étape Générique 23 (Améliorer le processus).
  - Entrées : Déroulement de la Review 2 et vécu d'équipe.
  - Travail d'application : Conduire l'analyse réflexive, constater l'efficacité de la levée de la dette d'empathie, et formaliser 2 axes d'amélioration pour S3.
  - Sortie (1 seul livrable) : `sprints/retrospective-2.md`.
