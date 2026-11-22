# Plan Préliminaire des Compétences (Sprint-Driven)

Boussole d'orientation pour la réalisation des **25 étapes du Flux Générique d'Ingénierie Logicielle** ([flux-travail-generique.md](../flux-travail/flux-travail-generique.md)).
Ce plan est une référence de départ : avant chaque étape, `skills-planer` critique cette prévision et propose la solution optimale.

---

## 1. Principes Directeurs
- **100% Itératif par Sprint :** Les skills sont créés uniquement au moment où le sprint en cours les exige.
- **Termes Théoriques Purs :** Respect strict des termes officiels du Design Thinking (*Empathie, Définition, Prototypage*) et de Scrum (*Sprint Planning, Daily, Review, Retrospective, Product Backlog*).
- **Tranches Verticales :** `developpement-laravel` prend en charge toute la fonctionnalité (TDD de bout en bout). Il intègre des sous-dossiers par couche (`layers/persistence`, `service`, `controller`, `interface`, `tests`) chargés dynamiquement.
- **Packages Métiers :** Les modules fonctionnels (ex: `package-articles` regroupant Articles + Catégories) encapsulent leurs règles et leur cartographie pour supprimer les relectures inutiles de code.

---

## 2. Cartographie Itérative par Sprint

### Sprint 0 : Cadrage, Design Thinking & Backlog Initial (Étapes 1 à 11)
- `init-depot` : Dépôt Git, arborescence standardisée et README racine (Étape 2).
- `cadrage-produit` : Périmètre In/Out SMART et justification de stack (Étapes 3, 4).
- `design-thinking-empathie` : Entretiens, Cartes d'Empathie, Personas (Étape 5).
- `design-thinking-definition` : Point of View (POV) et Vision Produit / Product Goal (Étape 6).
- `scrum-product-backlog` : User Stories INVEST, priorisation MoSCoW, Backlog Refinement (Étapes 7, 18).
- `design-thinking-prototypage` : UI Kit Preline UI, User Flow Mermaid et maquettes interactives (Étapes 8, 9, 19).
- `scrum-sprint-planning` : Cadrage timebox, engagement d'équipe et Sprint Planning (Étapes 1, 15).
- `scrum-sprint-review` : Démonstration incrément, test maquettes et décision Go/No-Go (Étapes 10, 22).
- `scrum-sprint-retrospective` : Bilan réflexif et plan d'amélioration continue (Étapes 11, 23).

### Sprint 1 : Socle Technique & Architecture (Étapes 12 à 14)
- `architecture-logicielle` : Schéma conceptuel erDiagram, 2 couches (MVC + Service) et ADR (Étape 12).
- `developpement-laravel` : Socle Laravel 13, persistance MySQL TodoList et première tranche verticale (Étapes 13, 14, 17, 21).

### Sprints N : Delivery Dual-Track & Packages Métiers (Étapes 15 à 23)
- `developpement-laravel` : Delivery vertical par fonctionnalité (TDD Red-Green-Refactor).
- `package-[domaine]` : Mémoire vive et règles de gestion par domaine :
  - `package-articles` (Articles + Catégories unifiés).
  - `package-auth-rbac` (Authentification et autorisations Spatie).
- `scrum-daily` : Synchronisation quotidienne debout de 15 min (Étape 20).

### Clôture de Projet : Déploiement & Bilan (Étapes 24 et 25)
- `deploiement-cloture` : Déploiement production, recette en ligne et bilan officiel de délibération (Étapes 24, 25).

---

## 3. Matrice de Couverture des 25 Étapes
- Étape 1 : `scrum-sprint-planning`
- Étape 2 : `init-depot`
- Étape 3 : `cadrage-produit`
- Étape 4 : `cadrage-produit`
- Étape 5 : `design-thinking-empathie`
- Étape 6 : `design-thinking-definition`
- Étape 7 : `scrum-product-backlog`
- Étape 8 : `design-thinking-prototypage`
- Étape 9 : `design-thinking-prototypage`
- Étape 10 : `scrum-sprint-review`
- Étape 11 : `scrum-sprint-retrospective`
- Étape 12 : `architecture-logicielle`
- Étape 13 : `developpement-laravel`
- Étape 14 : `developpement-laravel`
- Étape 15 : `scrum-sprint-planning`
- Étape 16 : `init-depot` / `realisation-sprint`
- Étape 17 : `developpement-laravel` (+ `package-articles` / `package-auth-rbac`)
- Étape 18 : `scrum-product-backlog`
- Étape 19 : `design-thinking-prototypage`
- Étape 20 : `scrum-daily`
- Étape 21 : `developpement-laravel`
- Étape 22 : `scrum-sprint-review`
- Étape 23 : `scrum-sprint-retrospective`
- Étape 24 : `deploiement-cloture`
- Étape 25 : `deploiement-cloture`
