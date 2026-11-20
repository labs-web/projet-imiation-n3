# Flux de Travail Opérationnel — Session S04 : Prototypage, Tests PHPUnit & Cycle de Vie

Ce document définit le flux de travail de la **Session S04** (Sprint 4) pour le niveau N3.
Il est structuré en **6 phases typées** (3 unités d'apprentissage **UA-Lab** et 3 blocs d'ingénierie opérationnelle **UA-Tâche**), totalisant **14 étapes de travail**.

---

## 1. Fiche d'Identification de la Session S04

- **Identifiant :** Session S04 (Sprint 4)
- **Titre :** Prototypage, Tests PHPUnit & Cycle de Vie des Articles
- **Durée indicative :** 80 heures (10 jours ouvrés) — *fournie à titre indicatif pour le concepteur et les formateurs*
- **Positionnement :** Quatrième sprint de delivery applicatif Dual-Track
- **Domaines de compétences mobilisés :**
  - Prototypage rapide et ergonomie utilisateur Preline UI (`D.311.1-design`)
  - Modélisation de machines à états finis en Mermaid (`D.311.2-uml`)
  - Middlewares et sécurité granulaire des routes (`D.312.1-architecture`)
  - Automatisation des tests unitaires sous PHPUnit (`D.321.1-laravel`)
- **Objectif global d'apprentissage :**
  - Préparer la branche Git `sprint-4` et actualiser la documentation projet.
  - Concevoir des maquettes interactives et prototypes validant l'expérience utilisateur sous **Preline UI**.
  - Modéliser les cycles de vie des articles (états de publication) en diagramme d'états déclaratif Mermaid.
  - Sécuriser les accès d'administration par middlewares et autorisations granulaires.
  - Automatiser sous **PHPUnit** la validation unitaire des classes de service métier (`ArticleServiceTest`) pour garantir la non-régression applicative.
  - Préparer la piste Discovery du Sprint 5 et clôturer le sprint par la démonstration et la rétrospective agile.

---

## 2. Organisation dans le Cadre Tri-Projets

- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas de la suite de tests unitaires PHPUnit et du cycle de vie des articles.
  - Alternance immédiate : chaque atelier théorique est mis en œuvre sur le Blog.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Phase de conception préalable ciblée (1h)** : Élaboration du diagramme d'états Mermaid et formalisation du plan de test unitaire.
  - **Épreuve sommative de Live Coding (40 min chrono sans assistance — 65% de la note finale du module)** : L'apprenant écrit et exécute une suite complète de tests PHPUnit sur les classes de service de son portfolio personnel.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Développement de la suite de tests unitaires et mise en place des middlewares de filtrage sur l'application métier.
  - Bilan réflexif et consolidation des acquis.

---

## 3. Épreuve de Live Coding (40 min chrono sans assistance — 65% de la note)

- **Contexte :** À partir du projet starter fourni (`dossier-depart/`), écrire en 40 minutes la classe de tests unitaire `ProjectServiceTest` validant l'ensemble des méthodes métier avec isolation des données.
- **Consignes opérationnelles :**
  - Créer le fichier de test unitaire dans `tests/Unit/Services/ProjectServiceTest.php`.
  - Écrire 3 cas de test indépendants : cas nominal, cas de filtrage sans résultat, et cas d'erreur attendue avec assertion d'exception.
  - Exécuter la suite avec `php artisan test --filter ProjectServiceTest` et obtenir 100% de passage au vert.
- **Critères d'évaluation :** Utilisation propre des assertions PHPUnit, isolation par transactions ou mocks, couverture des cas limites, code de test lisible.

---

## 4. Déroulement des 6 Phases de la Session S04

```mermaid
flowchart TD
    subgraph P1 ["Phase 1 : UA-Tâche Début — Planification du Sprint 4 & Préparation Git"]
        E1["Étape 1 : Planifier le Sprint 4"]
        E2["Étape 2 : Préparer l'environnement de sprint (Branche Git & README.md)"]
        E1 --> E2
    end

    subgraph P2 ["Phase 2 : UA-Lab — Prototypage Preline UI (D.311.1-design)"]
        E3["Étape 3 : Tutoriel-lab : Prototypage interactif et ergonomie Preline UI"]
        E4["Étape 4 : Tutoriel-application : Prototyper les flux d'administration"]
        E3 --> E4
    end

    subgraph P3 ["Phase 3 : UA-Lab — Machines à États Mermaid (D.311.2-uml)"]
        E5["Étape 5 : Tutoriel-lab : Modélisation de diagrammes d'états en Mermaid"]
        E6["Étape 6 : Tutoriel-application : Modéliser le cycle de vie des articles"]
        E5 --> E6
    end

    subgraph P4 ["Phase 4 : UA-Lab — Tests Unitaires PHPUnit (D.312.1 & D.321.1)"]
        E7["Étape 7 : Tutoriel-lab : Middlewares et automatisation de tests PHPUnit"]
        E8["Étape 8 : Tutoriel-application : Concevoir en détail et développer les tests"]
        E7 --> E8
    end

    subgraph P5 ["Phase 5 : UA-Tâche Milieu — Piste Discovery (Sprint 5)"]
        E9["Étape 9 : Affiner le Backlog pour le Sprint suivant"]
        E10["Étape 10 : Modéliser le User Flow et les maquettes du Sprint 5"]
        E9 --> E10
    end

    subgraph P6 ["Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité, Démonstration & Rétrospective"]
        E11["Étape 11 : Suivre l'avancement quotidien (Daily Scrum)"]
        E12["Étape 12 : Tester et valider l'Incrément (DoD)"]
        E13["Étape 13 : Présenter et inspecter (Sprint Review 4)"]
        E14["Étape 14 : Améliorer le processus (Sprint Retrospective 4)"]
        E11 --> E12 --> E13 --> E14
    end

    P1 --> P2 --> P3 --> P4 --> P5 --> P6
```

---

### Phase 1 : UA-Tâche Début — Planification du Sprint 4 et Préparation Git
*Cette phase rassemble les activités opérationnelles d'initialisation de l'itération sans nouvel apport conceptuel.*

- **Étape 1 : Planifier le Sprint 4**
  - Correspondance flux générique : Étape Générique 15 (Planifier le Sprint N).
  - Entrées : Product Backlog actualisé, retours de la Review 3 et actions de la Rétrospective S3.
  - Travail d'application sur le Blog : Chaque apprenant endosse le rôle de Product Owner pour son projet, définit le Sprint Goal S4 ("Sécuriser le cycle de vie des articles par middlewares et automatiser la suite de tests unitaires PHPUnit garantissant la non-régression"), décompose les tâches et valide le Sprint Backlog S4.
  - Sortie (1 seul livrable) : `scrum/sprint-backlog-s4.md`.
- **Étape 2 : Préparer l'environnement de sprint (Branche Git et README.md)**
  - Correspondance flux générique : Étape Générique 16 (Préparer l'environnement de sprint).
  - Entrées : Sprint Backlog S4 validé et branche `main`.
  - Travail d'application sur le Blog : Créer la branche Git `sprint-4` et actualiser la notice `README.md`.
  - Sortie (1 seul livrable) : `README.md`.

---

### Phase 2 : UA-Lab — Prototypage Rapide et Ergonomie Preline UI (Domaine D.311.1-design)
*Cette phase introduit les techniques de prototypage d'interface avec alternance directe apprentissage et application.*

- **Étape 3 : Tutoriel-lab : Prototypage interactif et ergonomie d'interface avec Preline UI**
  - Entrées : Composants de formulaires et modales Preline UI.
  - Notions de base à apprendre :
    - Principes d'utilisabilité : clarté des statuts système, prévention des erreurs, guidage visuel.
    - Prototypage interactif : modales de confirmation, tiroirs coulissants (*drawers*) et alertes contextuelles.
    - Évaluation heuristique d'interface selon les critères de Bastien et Scapin.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/design/guide-prototypage-preline.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/design/presentation-prototypage-preline.md`.
- **Étape 4 : Tutoriel-application : Prototyper les flux d'administration du Blog**
  - Entrées : User Stories d'administration et UI Kit Preline UI.
  - Travail d'application sur le Blog : Prototyper les flux de modération et de publication d'articles avec les composants interactifs Preline UI.
  - Sortie (1 seul livrable) : `docs/design/prototypes-administration.md`.

---

### Phase 3 : UA-Lab — Modélisation de Machines à États Finis en Mermaid (Domaine D.311.2-uml)
*Cette phase introduit la modélisation dynamique des états avec alternance directe apprentissage et application.*

- **Étape 5 : Tutoriel-lab : Modélisation de diagrammes d'états en syntaxe Mermaid**
  - Entrées : Guide de syntaxe Mermaid `stateDiagram-v2`.
  - Notions de base à apprendre :
    - Concepts d'état initial, état intermédiaire, état final et transitions déclenchées par un événement.
    - Gardes de transition et conditions logiques d'invalidation.
    - Syntaxe Mermaid `stateDiagram-v2` pour formaliser les changements de statuts.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/uml/guide-machines-etats-mermaid.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/uml/presentation-machines-etats-mermaid.md`.
- **Étape 6 : Tutoriel-application : Modéliser le cycle de vie de publication d'un article**
  - Entrées : Règles métiers du Blog et guide Mermaid.
  - Travail d'application sur le Blog : Modéliser le diagramme d'états complet d'un article : `Brouillon` $\to$ `EnRelecture` $\to$ `Publie` $\to$ `Archive`.
  - Sortie (1 seul livrable) : `docs/analyse/cycle-vie-articles.mmd`.

---

### Phase 4 : UA-Lab — Tests Unitaires Automatisés sous PHPUnit (Domaines D.312.1-architecture & D.321.1-laravel)
*Cette phase introduit l'automatisation des tests sous Laravel 13 avec alternance directe apprentissage et application.*

- **Étape 7 : Tutoriel-lab : Middlewares HTTP et automatisation de tests PHPUnit**
  - Entrées : Framework PHPUnit et environnement Laravel 13.
  - Notions de base à apprendre :
    - Configuration de `phpunit.xml` et environnement de test en mémoire.
    - Écriture de tests unitaires purs sur les classes Service avec mocks et stubs.
    - Assertions PHPUnit indispensables : `assertEquals`, `assertTrue`, `assertCount`, `expectException`.
    - Création et rattachement de middlewares HTTP personnalisés pour contrôler les statuts d'articles.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/laravel/guide-middlewares-tests-phpunit.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/laravel/presentation-middlewares-tests-phpunit.md`.
- **Étape 8 : Tutoriel-application : Concevoir en détail et développer les tests unitaires et le middleware**
  - Correspondance flux générique : Étape Générique 17 (Concevoir en détail et développer).
  - Entrées : Spécifications, diagramme d'états et compétences PHPUnit acquises.
  - Travail d'application sur le Blog :
    - *Projet d'Imitation :* Coder la suite de tests unitaires `ArticleServiceTest` couvrant 100% des méthodes de consultation, filtrage et transition d'états, et implémenter le middleware de contrôle des articles publiés.
    - *Projet Technique (Jour 8) :* Réaliser la conception préalable (diagramme d'états et plan de tests), puis coder et exécuter la suite de tests unitaires `ProjectServiceTest` sur son portfolio (Épreuve de Live Coding de 40 min).
    - *Projet Fil Rouge (Jours 9-10) :* Développer la suite de tests unitaires automatisés et middlewares sur l'application métier.
  - Sortie (1 seul livrable) : `tests/Unit/Services/ArticleServiceTest.php`.

---

### Phase 5 : UA-Tâche Milieu — Piste Discovery : Affinement du Backlog et Maquettage du Sprint 5
*Cette phase rassemble les activités d'ingénierie opérationnelle menées en temps masqué (~10% du temps) pour préparer le sprint suivant.*

- **Étape 9 : Affiner le Backlog pour le Sprint suivant**
  - Correspondance flux générique : Étape Générique 18 (Affiner le Backlog pour le Sprint suivant).
  - Entrées : Product Backlog et retours d'utilisation.
  - Travail d'application : Chaque apprenant, dans sa posture de Product Owner, clarifie les User Stories du Sprint 5 (Single Page Application réactive sous Alpine.js et tests d'utilisabilité SUS).
  - Sortie (1 seul livrable) : `scrum/backlog-refinement-s5.md`.
- **Étape 10 : Modéliser le User Flow et les maquettes du Sprint 5**
  - Correspondance flux générique : Étape Générique 19 (Modéliser le User Flow et maquetter pour le Sprint suivant).
  - Entrées : User Stories S5 et UI Kit Preline UI.
  - Travail d'application : Modéliser le parcours SPA sans rechargement et prototyper les maquettes interactives associées.
  - Sortie (1 seul livrable) : `docs/design/maquettes-sprint-5.md`.

---

### Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité DoD, Démonstration et Rétrospective
*Cette phase opérationnelle rassemble les rituels de clôture et l'amélioration continue.*

- **Étape 11 : Suivre l'avancement quotidien (Daily Scrum)**
  - Correspondance flux générique : Étape Générique 20 (Suivre l'avancement quotidien).
  - Entrées : Tableau Kanban du Sprint 4.
  - Travail d'application : Animer la réunion quotidienne debout de 15 minutes et synchroniser l'équipe.
  - Sortie (1 seul livrable) : `issues/issues-sprint-4.md`.
- **Étape 12 : Tester et valider l'Incrément (DoD)**
  - Correspondance flux générique : Étape Générique 21 (Tester et valider l'Incrément).
  - Entrées : Code source complet et rapport d'exécution des tests PHPUnit.
  - Travail d'application : Exécuter la checklist de validation (100% des tests PHPUnit au vert, transitions d'états conformes, zéro régression).
  - Sortie (1 seul livrable) : `docs/qualite/rapport-dod-sprint-4.md`.
- **Étape 13 : Présenter et inspecter (Sprint Review 4)**
  - Correspondance flux générique : Étape Générique 22 (Présenter et inspecter).
  - Entrées : Incrément logiciel S4 et maquettes du Sprint 5.
  - Travail d'application : Chaque apprenant anime la démonstration de son Incrément 4 en posture de Product Owner, valide la DoD et fait tester les maquettes de S5.
  - Sortie (1 seul livrable) : `sprints/pv-review-4.md`.
- **Étape 14 : Améliorer le processus (Sprint Retrospective 4)**
  - Correspondance flux générique : Étape Générique 23 (Améliorer le processus).
  - Entrées : Déroulement de la Review 4 et vécu d'équipe.
  - Travail d'application : Conduire l'analyse réflexive d'équipe, acter l'apport déterminant des tests automatisés, et planifier l'intégration d'Alpine.js pour S5.
  - Sortie (1 seul livrable) : `scrum/retrospective-s4.md`.
