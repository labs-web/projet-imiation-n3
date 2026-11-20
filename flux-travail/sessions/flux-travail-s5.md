# Flux de Travail Opérationnel — Session S05 : Tests Utilisateurs, SPA Alpine.js & API REST

Ce document définit le flux de travail de la **Session S05** (Sprint 5) pour le niveau N3.
Il est structuré en **6 phases typées** (3 unités d'apprentissage **UA-Lab** et 3 blocs d'ingénierie opérationnelle **UA-Tâche**), totalisant **14 étapes de travail**.

---

## 1. Fiche d'Identification de la Session S05

- **Identifiant :** Session S05 (Sprint 5)
- **Titre :** Tests Utilisateurs, SPA Alpine.js & API REST
- **Durée indicative :** 80 heures (10 jours ouvrés) — *fournie à titre indicatif pour le concepteur et les formateurs*
- **Positionnement :** Cinquième sprint de delivery applicatif Dual-Track
- **Domaines de compétences mobilisés :**
  - Protocoles de tests d'utilisabilité et score SUS (`D.311.1-design`)
  - Modélisation de contrats DTO et sérialisation JSON en Mermaid (`D.311.2-uml`)
  - Single Page Application réactive avec Alpine.js et Preline UI (`D.321.1-laravel`)
- **Objectif global d'apprentissage :**
  - Préparer la branche Git `sprint-5` et actualiser la documentation projet.
  - Conduire un protocole de tests d'utilisabilité (*Peer Testing*) et calculer le score System Usability Scale (SUS).
  - Modéliser les flux de données asynchrones, structures DTO et contrats JSON en syntaxe Mermaid.
  - Développer sous **Alpine.js** et **Preline UI** une interface réactive Single Page Application (SPA) avec filtrage asynchrone instantané sans aucun rechargement de page.
  - Préparer la piste Discovery du Sprint 6 et clôturer le sprint par la démonstration et la rétrospective agile.

---

## 2. Organisation dans le Cadre Tri-Projets

- **Jours 1 à 7 : Projet d'Imitation (*Blog des Lauréats*)**
  - Réalisation guidée pas-à-pas de l'expérience Single Page Application sous Alpine.js pour la recherche et le filtrage dynamique d'articles.
  - Alternance immédiate : chaque atelier théorique est mis en œuvre sur le Blog.
- **Jour 8 : Projet Technique (*Portfolio Développeur*)**
  - **Phase de conception préalable ciblée (1h)** : Élaboration du contrat JSON DTO et du diagramme de séquence Mermaid des échanges asynchrones.
  - **Épreuve sommative de Live Coding (40 min chrono sans assistance — 65% de la note finale du module)** : Dynamisation sous Alpine.js de la galerie de réalisations de son portfolio personnel sans aucun rechargement de page.
- **Jours 9 et 10 : Projet Fil Rouge (*Application Métier*, ex : Gestion de Cinéma)**
  - Développement de l'interface dynamique SPA avec Alpine.js connectée aux endpoints REST JSON sur l'application métier.
  - Bilan réflexif et consolidation des acquis.

---

## 3. Épreuve de Live Coding (40 min chrono sans assistance — 65% de la note)

- **Contexte :** À partir du projet starter fourni (`dossier-depart/`), implémenter en 40 minutes le composant de filtrage en temps réel des projets du portfolio sous Alpine.js (`x-data`, `fetch()`, `x-for`) avec styles Preline UI.
- **Consignes opérationnelles :**
  - Créer la route API `/api/realisations` retournant les données au format JSON structuré.
  - Coder le composant Alpine.js avec initialisation d'état réactif et gestion du spinner de chargement.
  - Implémenter le filtrage instantané par catégorie avec mise à jour du DOM sans rechargement.
- **Critères d'évaluation :** Réactivité fluide, gestion propre du cycle de vie asynchrone, intégration Preline UI, code sans console warnings.

---

## 4. Déroulement des 6 Phases de la Session S05

```mermaid
flowchart TD
    subgraph P1 ["Phase 1 : UA-Tâche Début — Planification du Sprint 5 & Préparation Git"]
        E1["Étape 1 : Planifier le Sprint 5"]
        E2["Étape 2 : Préparer l'environnement de sprint (Branche Git & README.md)"]
        E1 --> E2
    end

    subgraph P2 ["Phase 2 : UA-Lab — Tests Utilisabilité & SUS (D.311.1-design)"]
        E3["Étape 3 : Tutoriel-lab : Protocoles de tests d'utilisabilité et SUS"]
        E4["Étape 4 : Tutoriel-application : Conduire la campagne de tests sur le Blog"]
        E3 --> E4
    end

    subgraph P3 ["Phase 3 : UA-Lab — DTO & JSON Mermaid (D.311.2-uml)"]
        E5["Étape 5 : Tutoriel-lab : Modélisation des contrats DTO et flux JSON"]
        E6["Étape 6 : Tutoriel-application : Modéliser les contrats API du Blog"]
        E5 --> E6
    end

    subgraph P4 ["Phase 4 : UA-Lab — Single Page App Alpine.js (D.321.1-laravel)"]
        E7["Étape 7 : Tutoriel-lab : Dynamisation SPA avec Alpine.js et Preline UI"]
        E8["Étape 8 : Tutoriel-application : Concevoir en détail et développer la SPA"]
        E7 --> E8
    end

    subgraph P5 ["Phase 5 : UA-Tâche Milieu — Piste Discovery (Sprint 6)"]
        E9["Étape 9 : Affiner le Backlog pour le Sprint suivant"]
        E10["Étape 10 : Modéliser le User Flow et les maquettes du Sprint 6"]
        E9 --> E10
    end

    subgraph P6 ["Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité, Démonstration & Rétrospective"]
        E11["Étape 11 : Suivre l'avancement quotidien (Daily Scrum)"]
        E12["Étape 12 : Tester et valider l'Incrément (DoD)"]
        E13["Étape 13 : Présenter et inspecter (Sprint Review 5)"]
        E14["Étape 14 : Améliorer le processus (Sprint Retrospective 5)"]
        E11 --> E12 --> E13 --> E14
    end

    P1 --> P2 --> P3 --> P4 --> P5 --> P6
```

---

### Phase 1 : UA-Tâche Début — Planification du Sprint 5 et Préparation Git
*Cette phase rassemble les activités opérationnelles d'initialisation de l'itération sans nouvel apport conceptuel.*

- **Étape 1 : Planifier le Sprint 5**
  - Correspondance flux générique : Étape Générique 15 (Planifier le Sprint N).
  - Entrées : Product Backlog actualisé, retours de la Review 4 et actions de la Rétrospective S4.
  - Travail d'application sur le Blog : Chaque apprenant endosse le rôle de Product Owner pour son projet, définit le Sprint Goal S5 ("Transformer la consultation et le filtrage d'articles en une expérience Single Page Application fluide sous Alpine.js avec validation ergonomique par score SUS"), décompose les tâches et valide le Sprint Backlog S5.
  - Sortie (1 seul livrable) : `scrum/sprint-backlog-s5.md`.
- **Étape 2 : Préparer l'environnement de sprint (Branche Git et README.md)**
  - Correspondance flux générique : Étape Générique 16 (Préparer l'environnement de sprint).
  - Entrées : Sprint Backlog S5 validé et branche `main`.
  - Travail d'application sur le Blog : Créer la branche Git `sprint-5` et mettre à jour le fichier `README.md`.
  - Sortie (1 seul livrable) : `README.md`.

---

### Phase 2 : UA-Lab — Protocoles de Tests d'Utilisabilité et Score SUS (Domaine D.311.1-design)
*Cette phase introduit la mesure quantitative de l'utilisabilité avec alternance directe apprentissage et application.*

- **Étape 3 : Tutoriel-lab : Protocoles de tests d'utilisabilité et mesure du score SUS**
  - Entrées : Méthodologie du questionnaire System Usability Scale (SUS).
  - Notions de base à apprendre :
    - Protocole d'évaluation par les pairs (*Peer Testing*) : consignes neutres, tâches scénarisées, chronométrage.
    - Grille standardisée des 10 questions du test SUS (alternance items positifs et négatifs).
    - Méthode de calcul du score normalisé sur 100 et interprétation ergonomique.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/design/guide-tests-utilisabilite-sus.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/design/presentation-tests-utilisabilite-sus.md`.
- **Étape 4 : Tutoriel-application : Conduire la campagne de tests sur le Blog**
  - Entrées : Incrément logiciel disponible et formulaire SUS.
  - Travail d'application sur le Blog : Faire tester le Blog des Lauréats par 5 apprenants pairs, calculer le score SUS moyen et formaliser les recommandations ergonomiques.
  - Sortie (1 seul livrable) : `docs/design/rapport-sus-blog.md`.

---

### Phase 3 : UA-Lab — Modélisation de Contrats DTO et Sérialisation JSON en Mermaid (Domaine D.311.2-uml)
*Cette phase introduit la formalisation des échanges API asynchrones avec alternance directe apprentissage et application.*

- **Étape 5 : Tutoriel-lab : Modélisation des contrats DTO et flux JSON en Mermaid**
  - Entrées : Guide Mermaid `sequenceDiagram` et `classDiagram`.
  - Notions de base à apprendre :
    - Patron Data Transfer Object (DTO) : découplage entre modèle de base de données et charge utile JSON.
    - Diagramme de séquence Mermaid représentant les requêtes AJAX `fetch()`, le statut HTTP 200 et les structures de réponse.
    - Formatage normalisé des erreurs asynchrones (status 422, payload JSON d'erreurs).
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/uml/guide-dto-json-mermaid.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/uml/presentation-dto-json-mermaid.md`.
- **Étape 6 : Tutoriel-application : Modéliser les contrats API du Blog**
  - Entrées : Guide Mermaid et besoins de recherche dynamique.
  - Travail d'application sur le Blog : Modéliser le contrat de données DTO retourné par l'endpoint `/api/articles` et le diagramme de séquence des échanges asynchrones.
  - Sortie (1 seul livrable) : `docs/analyse/contrat-api-articles.mmd`.

---

### Phase 4 : UA-Lab — Single Page Application Réactive avec Alpine.js et Preline UI (Domaine D.321.1-laravel)
*Cette phase introduit la dynamisation client réactive avec alternance directe apprentissage et application.*

- **Étape 7 : Tutoriel-lab : Dynamisation SPA avec Alpine.js et Preline UI**
  - Entrées : Bibliothèque Alpine.js et Preline UI.
  - Notions de base à apprendre :
    - Directives réactives essentielles : `x-data`, `x-init`, `x-bind`, `x-on:click`, `x-model`, `x-show`, `x-for`.
    - Appels asynchrones avec `fetch()` vers les endpoints JSON Laravel avec gestion du statut de chargement (*loading state*).
    - Manipulation fluide du DOM et transition d'affichage avec les classes utilitaires Preline UI.
  - Sorties de l'atelier d'apprentissage (2 livrables) :
    - Guide explicatif détaillé : `tutoriels/laravel/guide-spa-alpine-preline.md`.
    - Support de présentation au format Marp Markdown : `tutoriels/laravel/presentation-spa-alpine-preline.md`.
- **Étape 8 : Tutoriel-application : Concevoir en détail et développer la SPA de consultation d'articles**
  - Correspondance flux générique : Étape Générique 17 (Concevoir en détail et développer).
  - Entrées : Spécifications, contrats DTO et compétences Alpine.js acquises.
  - Travail d'application sur le Blog :
    - *Projet d'Imitation :* Coder l'endpoint JSON `/api/articles` avec filtrage par catégorie et mot-clé, et implémenter la vue SPA sous Alpine.js et Preline UI sans aucun rechargement de page.
    - *Projet Technique (Jour 8) :* Réaliser la conception préalable (contrat DTO et diagramme de séquence), puis dynamiser sous Alpine.js la galerie de réalisations de son portfolio personnel (Épreuve de Live Coding de 40 min).
    - *Projet Fil Rouge (Jours 9-10) :* Développer l'interface réactive SPA Alpine.js connectée aux endpoints REST sur l'application métier.
  - Sortie (1 seul livrable) : `resources/views/articles/index-spa.blade.php`.

---

### Phase 5 : UA-Tâche Milieu — Piste Discovery : Affinement du Backlog et Maquettage du Sprint 6
*Cette phase rassemble les activités d'ingénierie opérationnelle menées en temps masqué (~10% du temps) pour préparer le sprint suivant.*

- **Étape 9 : Affiner le Backlog pour le Sprint suivant**
  - Correspondance flux générique : Étape Générique 18 (Affiner le Backlog pour le Sprint suivant).
  - Entrées : Product Backlog et retours d'utilisation.
  - Travail d'application : Chaque apprenant, dans sa posture de Product Owner, clarifie les User Stories du Sprint 6 (Sécurité Spatie RBAC et démarche TDD complète).
  - Sortie (1 seul livrable) : `scrum/backlog-refinement-s6.md`.
- **Étape 10 : Modéliser le User Flow et les maquettes du Sprint 6**
  - Correspondance flux générique : Étape Générique 19 (Modéliser le User Flow et maquetter pour le Sprint suivant).
  - Entrées : User Stories S6 et UI Kit Preline UI.
  - Travail d'application : Modéliser les parcours d'administration RBAC et prototyper les maquettes interactives associées.
  - Sortie (1 seul livrable) : `docs/design/maquettes-sprint-6.md`.

---

### Phase 6 : UA-Tâche Fin — Suivi Quotidien, Qualité DoD, Démonstration et Rétrospective
*Cette phase opérationnelle rassemble les rituels de clôture et l'amélioration continue.*

- **Étape 11 : Suivre l'avancement quotidien (Daily Scrum)**
  - Correspondance flux générique : Étape Générique 20 (Suivre l'avancement quotidien).
  - Entrées : Tableau Kanban du Sprint 5.
  - Travail d'application : Animer la réunion debout quotidienne de 15 minutes et synchroniser l'équipe.
  - Sortie (1 seul livrable) : `issues/issues-sprint-5.md`.
- **Étape 12 : Tester et valider l'Incrément (DoD)**
  - Correspondance flux générique : Étape Générique 21 (Tester et valider l'Incrément).
  - Entrées : Code source complet et métriques de performance SPA.
  - Travail d'application : Exécuter la checklist de validation (filtrage instantané fluide sans rechargement, absence d'erreurs console, score SUS $\ge 70$).
  - Sortie (1 seul livrable) : `docs/qualite/rapport-dod-sprint-5.md`.
- **Étape 13 : Présenter et inspecter (Sprint Review 5)**
  - Correspondance flux générique : Étape Générique 22 (Présenter et inspecter).
  - Entrées : Incrément logiciel S5 et maquettes du Sprint 6.
  - Travail d'application : Chaque apprenant anime la démonstration de son Incrément 5 en posture de Product Owner, présente le score SUS et fait tester les maquettes de S6.
  - Sortie (1 seul livrable) : `sprints/pv-review-5.md`.
- **Étape 14 : Améliorer le processus (Sprint Retrospective 5)**
  - Correspondance flux générique : Étape Générique 23 (Améliorer le processus).
  - Entrées : Déroulement de la Review 5 et vécu d'équipe.
  - Travail d'application : Conduire l'analyse réflexive d'équipe, acter l'excellence du ressenti utilisateur sous Alpine.js, et préparer l'implémentation de Spatie RBAC pour S6.
  - Sortie (1 seul livrable) : `scrum/retrospective-s5.md`.
