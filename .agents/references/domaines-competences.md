---
version: "1.2.0"
description: "Référentiel officiel et source unique de vérité (SSOT) des domaines de compétences, codes normalisés, slugs canoniques et règles d'exclusion de l'ingénierie didactique."
---

# Référentiel des Domaines de Compétences et Slugs Officiels

Ce document constitue la **source unique de vérité (SSOT)** définissant l'ensemble des domaines de compétences mobilisés dans les projets de formation, leurs identifiants normalisés et leurs slugs de répertoires officiels.

Tous les agents IA (en particulier l'**Agent Concepteur de Session** et l'**Agent Réalisation de Sprint**) ainsi que les fichiers de session (`flux-travail/sessions/flux-travail-s*.md`) doivent obligatoirement utiliser les slugs et codes définis ci-dessous.

---

## 1. Règle d'Attribution des Codes Officiels `UA.*`

> [!IMPORTANT]
> Les codes officiels d'Unités d'Apprentissage (`UA.xxx.xx`) proviennent de l'**Agent Autoformation**.  
> **Règle formelle :** Un code `UA.*` est attribué à une unité d'apprentissage ou un tutoriel **uniquement lorsqu'il passe à l'état réalisé**.  
> Tant qu'une unité d'apprentissage est en cours de conception, de planification ou non encore réalisée, elle est identifiée par son libellé descriptif normalisé sans code `UA.*` prématuré.

---

## 2. Cartographie des Domaines de Compétences

### 1. Méthodes Agiles Scrum (`scrum`)
- **Code officiel :** `D.351.1-scrum`
- **Slug de répertoire canonique :** `scrum` (ex : `tutoriels/scrum/`)
- **Compétence associée :** `C.351` — Gouverner les rituels agiles et les cérémonies de sprint Scrum.
- **Périmètre d'ingénierie :** Cadre Scrum, Manifeste Agile, Rôles (PO, SM, Développeurs), 5 événements, 3 artéfacts, Definition of Done, Product Backlog, User Stories INVEST, MoSCoW, Burndown chart.
- **Sessions mobilisatrices :** Session S0 (initiation collective avec Groupe 1 PO), puis toutes les sessions S1 à S8 (pilotage de sprint par chaque apprenant en rôle PO).

---

### 2. Conception & Design Thinking (`design`)
- **Code officiel :** `D.311.1-design`
- **Slug de répertoire canonique :** `design` (ex : `tutoriels/design/`)
- **Compétence associée :** `C.311` — Concevoir des interfaces centrées utilisateur et conduire la démarche ergonomique.
- **Unités d'apprentissage de référence :**
  - Unité 1 : Démarche de Design Thinking (Double Diamant, divergence / convergence).
  - Unité 2 : Empathie (immersion terrain, entretiens semi-directifs, Carte d'Empathie 4 quadrants, Personas et scénarios d'usage).
  - Unité 3 : Modélisation de parcours utilisateur (User Flow déclaratif).
  - Unité 4 : Prototypage d'interface (incluant l'UI Kit, composants d'interface, ergonomie, maquettes interactives et tests d'utilisabilité SUS).
- **Périmètre d'ingénierie :** Modèle du Double Diamant, Immersion terrain, Entretiens semi-directifs, Carte d'Empathie, Fiches Personas, Scénarios d'usage, Formulation POV / HMW, Modélisation déclarative de User Flow, UI Kit et composants d'interface, Tests d'utilisabilité par les pairs (*Peer Testing*) et score normalisé SUS.
- **Sessions mobilisatrices :** Sessions S0, S2, S3, S4, S5.

---

### 3. Modélisation UML & Conception Technique (`uml`)
- **Code officiel :** `D.311.2-uml`
- **Slug de répertoire canonique :** `uml` (ex : `tutoriels/uml/`)
- **Compétence associée :** `C.311` — Modéliser fonctionnellement et techniquement une solution logicielle.
- **Règle terminologique :** Le terme *Mermaid* ne doit pas être utilisé dans les titres de domaines ou d'unités d'apprentissage. Mermaid est un **outil textuel de rendu** utilisé pour apporter une solution technique dans un tutoriel, non un concept d'ingénierie.
- **Périmètre d'ingénierie :** Diagrammes structurels et comportementaux de conception logicielle (diagrammes de contexte, cas d'utilisation macro `<<include>>`, `<<extend>>`, diagrammes de classes du domaine pur, relations Many-to-Many `erDiagram`, machines à états finis `stateDiagram-v2`, diagrammes de séquence et contrats DTO `sequenceDiagram`, matrice d'habilitation RBAC).
- **Sessions mobilisatrices :** Sessions S1, S2, S3, S4, S5, S6.

---

### 4. Architecture Logicielle (`architecture`)
- **Code officiel :** `D.312.1-architecture`
- **Slug de répertoire canonique :** `architecture` (ex : `tutoriels/architecture/`)
- **Compétence associée :** `C.312` — Concevoir et structurer une architecture logicielle modulaire et découplée.
- **Périmètre d'ingénierie :** Architecture en deux couches (Contrôleurs minces HTTP + Couche Service métier indépendante), Inversion de Contrôle (IoC) et injection de dépendance, formalisation des décisions architecturales par Architectural Decision Records (ADR), intercepteurs HTTP (Middlewares), contrôle d'accès standardisé (Spatie Laravel-Permission).
- **Sessions mobilisatrices :** Sessions S1, S2, S3, S4, S6.

---

### 5. Développement Backend Laravel & Persistance Relationnelle (`laravel`)
- **Code officiel :** `D.321.1-laravel`
- **Slug de répertoire canonique :** `laravel` (ex : `tutoriels/laravel/`)
- **Compétence associée :** `C.321` — Développer des applications Web robustes avec un framework moderne et persistance relationnelle.
- **Périmètre d'ingénierie :** Framework Laravel 13, ORM Eloquent, Migrations et Seeders MySQL, Routage dynamique, Validation sémantique par `FormRequest`, Vues réactives Blade et Tailwind CSS avec Preline UI, Dynamisation Single Page Application avec Alpine.js et endpoints JSON, Tests automatisés PHPUnit, Démarche TDD (Red-Green-Refactor).
- **Sessions mobilisatrices :** Sessions S1, S2, S3, S4, S5, S6, S8.

---

### 6. Développement Client Mobile Android Natif (`mobile`)
- **Code officiel :** `D.323.1-mobile`
- **Slug de répertoire canonique :** `mobile` (ex : `tutoriels/mobile/`)
- **Compétence associée :** `C.323` — Développer une application mobile native connectée à une API RESTful.
- **Périmètre d'ingénierie :** Langage Kotlin (null-safety, data classes, Coroutines avec `Dispatchers.IO`), UI déclarative avec Jetpack Compose (Scaffold, LazyColumn, State hoisting), Navigation multi-écrans avec `NavHost`, Client HTTP Retrofit 2 avec convertisseur Moshi, Patron d'architecture MVVM (ViewModel, StateFlow).
- **Sessions mobilisatrices :** Session S7.

---

### 7. Déploiement en Production, DevOps & Portabilité (`devops`)
- **Code officiel :** `D.341.1-devops`
- **Slug de répertoire canonique :** `devops` (ex : `tutoriels/devops/`)
- **Compétence associée :** `C.341` — Packager, tester et déployer une solution logicielle en environnement de production.
- **Périmètre d'ingénierie :** Cahier de recette globale de bout en bout (E2E), Déploiement distant sans interruption de service (*Zero-Downtime Deployment*), Configuration sécurisée des variables d'environnement, Optimisation des caches, Certificats HTTPS, Packaging autonome multiplateforme avec NativePHP (Desktop / Mobile embarqué), Soutenance officielle de qualification N3.
- **Sessions mobilisatrices :** Session S8.

---

### 8. Réalisation et Conduite de Projet (`realisation-projet`)
- **Code officiel :** `D.351.2-realisation-projet`
- **Slug de répertoire canonique :** `realisation-projet` (ex : `tutoriels/realisation-projet/`)
- **Compétence associée :** `C.351` — Cadrer, conduire et livrer un projet d'ingénierie logicielle.
- **Périmètre d'ingénierie :** Note de cadrage (objectifs SMART, périmètre In/Out), Justification technique de stack, Rituels de clôture de sprint (Sprint Review avec démonstration de l'Incrément, audit des 7 critères de la Definition of Done, Rétrospective réflexive, Affinement du backlog), Bilan global de capitalisation.
- **Sessions mobilisatrices :** Transverse à l'ensemble des sessions S0 à S8.

---

## 3. Règle d'Exclusion Définitive du Domaine IA Apprenant

> [!WARNING]
> Conformément à l'arbitrage officiel du concepteur, l'ancien domaine **`D.325.1-ia`** (et la compétence `C.325`) portant sur la création d'Agents IA, la rédaction de prompts et l'architecture de skills par l'apprenant est **définitivement supprimé** de l'ensemble du cursus de formation.  
> L'Agent IA Antigravity intervient exclusivement comme **outil copilote et d'assistance méthodologique** pour le concepteur et l'apprenant, mais ne constitue en aucun cas un domaine d'apprentissage ou d'évaluation pour les apprenants.

---

## 4. Matrice de Correspondance Résumée

- **Scrum :** Code `D.351.1-scrum` | Slug dossier `scrum` | Skill associé `domaine-scrum`
- **Design Thinking & Prototypage :** Code `D.311.1-design` | Slug dossier `design`
- **Modélisation UML :** Code `D.311.2-uml` | Slug dossier `uml`
- **Architecture Logicielle :** Code `D.312.1-architecture` | Slug dossier `architecture`
- **Laravel Backend :** Code `D.321.1-laravel` | Slug dossier `laravel`
- **Mobile Android :** Code `D.323.1-mobile` | Slug dossier `mobile`
- **DevOps & Packaging :** Code `D.341.1-devops` | Slug dossier `devops`
- **Conduite de Projet :** Code `D.351.2-realisation-projet` | Slug dossier `realisation-projet` | Skill associé `cloture-sprint`
