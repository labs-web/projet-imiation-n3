# Flux de Travail Pédagogique des Sessions de Formation

Ce document transpose le [Flux de Travail Générique d'Ingénierie Logicielle](./flux-travail-generique.md) dans le cadre didactique de la formation Solicode Niveau 3.

Il organise la réalisation des Sprints pédagogiques par compétences, en fournissant à l'apprenant et à l'Agent IA le cadre normalisé des étapes d'apprentissage.

---

## 1. Cadre Didactique du Sprint 1

- **Nom de la session** : Sprint 1 — Initialisation, Cadrage & Première Fonctionnalité Laravel
- **Durée réglementaire** : 80 heures (2 semaines).
- **Branche Git partagée** : `sprint1`.
- **Compétences associées** :
  - `C.311` : Modéliser une application informatique avec UML Mermaid.
  - `C.312` : Concevoir une architecture logicielle découplée.
  - `C.321` : Développer des composants d'interface et une logique backend avec Laravel.
  - `C.325` : Outiller l'environnement avec un Agent IA et concevoir des skills.
  - `C.351` : Piloter un projet de développement selon la méthode agile Scrum.

---

## 2. Déroulement Pédagogique des Étapes du Sprint 1

Chaque étape pédagogique instancie une étape du flux générique et respecte rigoureusement la structure normalisée à 4 sections.

---

### Étape 1 : Initialisation du Dépôt et Structure Documentaire
*(Référence générique : Étape 5 — Préparation de l'environnement technique)*

#### Base théorique et pratique
- Utilisation de GitHub CLI (`gh repo create`) et conventions de branches (`sprint[N]`).
- Structuration modulaire des dossiers documentaires et script d'automatisation Node.js.

#### Prérequis
- Présentation et cadrage du projet d'imitation par le formateur référent ESSARRAJ Fouad.

#### Travail à faire
- Créer le dépôt local Git, configurer `.gitignore` et réaliser le premier commit.
- Publier le dépôt distant sur GitHub via GitHub CLI sur la branche `sprint1`.
- Rédiger le fichier `README.md` racine selon le modèle officiel Solicode.
- Créer le dossier racine `presentations/` avec son `README.md` et les fichiers diaporamas vides (`presentation-blog.md`, `presentation-sprint1.md`) au format Marp.
- Créer le dossier racine `rapport/` avec son `README.md`, le document consolidé `rapport-blog.md`, le sous-dossier `chapitres/` et le script Node.js autonome `concat-chapitres.js`.

#### Livrables
- Dépôt GitHub distant publié et synchronisé sur la branche `sprint1`.
- Fichier `README.md` racine conforme.
- Dossier du code source `src/` avec son `README.md`.
- Dossier `presentations/` avec son `README.md` et ses diaporamas Marp.
- Dossier `rapport/` avec son `README.md` et son script `concat-chapitres.js`.

---

### Étape 2 : Initialisation de l'Agent IA et Règles Always-On
*(Référence générique : Étape 5 — Socle technique & outillage de développement)*

#### Base théorique et pratique
- `UA.325.11` : Initialisation de l'Agent IA et Architecture des Skills.
- Formulation de consignes RIO, posture agentique et règles Always-On.
- Tutoriels associés : `tutoriels/ia/agent-skills/prompt-engineering/` et `tutoriels/ia/agent-skills/agent-ia/`.

#### Prérequis
- Dépôt Git initialisé et arborescence documentaire créée sur la branche `sprint1` (Étape 1).

#### Travail à faire
- Définir le socle commun des règles et contexte du projet : `.agents/rules/contexte-projet.md` et `.agents/rules/regles-generales.md`.
- Déployer les compétences agentiques initiales : `.agents/skills/skills-dev/` et `.agents/skills/gestion-depot/`.
- Configurer l'environnement pour la découverte native des skills par l'Agent IA.
- Rédiger les fiches de synthèse théoriques et diaporamas Marp associés.

#### Livrables
- Fiches de synthèse et présentations Marp dans `tutoriels/ia/agent-skills/`.
- Règles permanentes : `.agents/rules/contexte-projet.md` et `.agents/rules/regles-generales.md`.
- Skills agentiques initiaux : `.agents/skills/skills-dev/` et `.agents/skills/gestion-depot/`.
- Enregistrement des versions dans `.sync/tutoriels/ia/agent-skills/.../version.yml`.

---

### Étape 3 : Formalisation des Flux de Travail et Référentiels
*(Référence générique : Cadrage méthodologique global)*

#### Base théorique et pratique
- Démarche unifiée : Design Thinking, Gestion de Projet, Processus OO et Scrum Dual-Track.
- Formalisation des processus d'ingénierie logicielle et des étapes didactiques.

#### Prérequis
- Initialisation de l'Agent IA terminée (Étape 2).

#### Travail à faire
- Formaliser le flux d'ingénierie générique dans `flux-travail/flux-travail-generique.md`.
- Formaliser le flux d'apprentissage pédagogique dans `flux-travail/flux-travail-pedagogique.md`.
- Élaborer les 5 guides méthodologiques thématiques dans `flux-travail/docs/`.
- Configurer le skill de gouvernance : `.agents/skills/flux-travail/SKILL.md`.

#### Livrables
- Fichier `flux-travail/flux-travail-generique.md`.
- Fichier `flux-travail/flux-travail-pedagogique.md`.
- Les 5 guides de référence dans `flux-travail/docs/`.
- Skill d'accompagnement : `.agents/skills/flux-travail/SKILL.md`.

---

### Étape 4 : Cadrage du Projet sous Gouvernance Scrum
*(Référence générique : Étape 1 & Étape 2 — Planification et Cadrage)*

#### Base théorique et pratique
- `UA.351.11` : Initiation à la méthode Agile Scrum.
- Piliers Scrum, rôles de l'équipe, timebox de sprint et charte d'engagement.
- Tutoriels associés : `tutoriels/scrum/initiation-scrum/comprendre-scrum/` et `tutoriels/scrum/initiation-scrum/vision-besoins/`.

#### Prérequis
- Référentiels de flux de travail validés (Étape 3).

#### Travail à faire
- Formaliser le fichier de planification des sprints : `sprints/sprints.md`.
- Activer le Sprint 1 avec sa vision, ses acteurs cibles, son périmètre in/out et sa branche Git `sprint1`.
- Consigner les commandes de cadrage dans `tutoriels/realisation-projet/cadrage/perimetre-produit/perimetre-produit.command.md`.
- Rédiger les fiches de synthèse et présentations Marp de cadrage Scrum.

#### Livrables
- Fichier de gouvernance Scrum : `sprints/sprints.md` et son guide `sprints/README.md`.
- Fiches de synthèse et diaporamas Marp dans `tutoriels/scrum/initiation-scrum/`.
- Enregistrement des versions dans `.sync/tutoriels/scrum/initiation-scrum/.../version.yml`.

---

### Étape 5 : Structuration du Product Backlog et des Issues de Sprint
*(Référence générique : Étape 3 — Définition & Product Backlog)*

#### Base théorique et pratique
- `UA.351.11` : Initiation à la méthode Agile Scrum (Gestion du Backlog).
- Rédaction de User Stories INVEST avec critères d'acceptation et priorisation de sprint.
- Tutoriels associés : `tutoriels/scrum/initiation-scrum/product-backlog/` et `tutoriels/scrum/initiation-scrum/sprint-planning-execution/`.

#### Prérequis
- Cadrage Scrum du Sprint 1 formalisé (Étape 4).

#### Travail à faire
- Créer l'espace de suivi opérationnel : dossier `issues/`.
- Décomposer le périmètre du Sprint 1 en User Stories et tâches techniques.
- Organiser les issues par statut (`issues/issues-open.md`, `issues/issues-à-valider.md`, `issues/issues-closes.md`).
- Rédiger la fiche de synthèse et la présentation Marp associées à la gestion du Backlog.

#### Livrables
- Dossier `issues/` avec son `README.md` et ses fichiers de suivi des tâches.
- Fiches de synthèse et présentations Marp dans `tutoriels/scrum/initiation-scrum/product-backlog/`.
- Enregistrement des versions dans `.sync/`.

---

### Étape 6 : Modélisation UML Mermaid du Contexte et des Cas d'Utilisation
*(Référence générique : Étape 5 — Architecture & Modélisation)*

#### Base théorique et pratique
- `UA.311.21` : Modélisation du Système d'Information avec diagrammes Mermaid textuels.
- Diagramme de contexte système et diagramme de cas d'utilisation (Use Case).

#### Prérequis
- User Stories et tâches du Sprint 1 recensées dans `issues/` (Étape 5).

#### Travail à faire
- Modéliser le diagramme de contexte du système *Blog des Lauréats* (utilisateurs, administrateurs, visiteurs).
- Modéliser le diagramme de cas d'utilisation pour la consultation des articles.
- Déposer les diagrammes dans `docs/modelisation/` avec leur guide `docs/README.md`.

#### Livrables
- Fiches de modélisation Mermaid : `docs/modelisation/contexte.md` et `docs/modelisation/cas-utilisation.md`.
- Guide du dossier : `docs/README.md`.

---

### Étape 7 : Conception de l'Architecture Logicielle en 2 Couches
*(Référence générique : Étape 5 — Conception de l'architecture)*

#### Base théorique et pratique
- `UA.312.11` : Architecture en 2 Couches (Contrôleur mince -> Classe Service).
- Découplage des responsabilités, testabilité et robustesse du code.

#### Prérequis
- Modélisation des cas d'utilisation validée (Étape 6).

#### Travail à faire
- Définir le pattern architectural : `ArticleController` (Contrôleur mince HTTP) injectant `ArticleService` (Classe Service métier).
- Spécifier les signatures des méthodes de récupération d'un article.
- Documenter le principe d'architecture dans `docs/architecture/architecture-2-couches.md`.

#### Livrables
- Fiche de conception : `docs/architecture/architecture-2-couches.md`.

---

### Étape 8 : Implémentation sous Laravel 12 de la Consultation d'un Article
*(Référence générique : Étape 9 & Étape 12 — Développement et Tests de l'Incrément)*

#### Base théorique et pratique
- `UA.321.11` : Développement Backend et Gabarits Frontend sous Laravel 12.
- Routage web dynamique, injection de dépendance, gabarit Blade responsive sous Tailwind CSS et gestion de l'erreur HTTP 404.

#### Prérequis
- Conception de l'architecture 2 couches validée (Étape 7).

#### Travail à faire
- Configurer la route dynamique dans `src/routes/web.php`.
- Implémenter le contrôleur mince `ArticleController` dans `src/app/Http/Controllers/`.
- Développer la classe Service `ArticleService` dans `src/app/Services/`.
- Traiter explicitement la ressource introuvable avec déclenchement d'une erreur 404 propre.
- Concevoir la vue Blade responsive pour l'affichage de l'article dans `src/resources/views/`.
- Vérifier manuellement le bon affichage responsive et les cas d'erreur.

#### Livrables
- Code source complet sous `src/` : route, contrôleur, service et vue Blade responsive.
- Gestion fonctionnelle de l'erreur 404.
- Page de consultation détaillée d'un article opérationnelle et testée.

---

### Étape 9 : Clôture du Sprint 1 et Rituels Agiles
*(Référence générique : Étape 13 & Étape 14 — Sprint Review et Sprint Retrospective)*

#### Base théorique et pratique
- `UA.351.11` : Rituels de fin de sprint Scrum (Sprint Review, Rétrospective réflexive, Débriefing).
- Démonstration de l'Incrément logiciel, bilan d'apprentissage et amélioration continue.
- Skill modulaire associé : `.agents/skills/cloture-sprint/`.

#### Prérequis
- Fonctionnalité de consultation d'article implémentée et testée (Étape 8).

#### Travail à faire
- Animer la Sprint Review pour démontrer l'Incrément logiciel opérationnel.
- Conduire la Rétrospective réflexive et consigner les actions d'amélioration.
- Exécuter le skill `/cloture-sprint` pour auditer les livrables et la Definition of Done.
- Finaliser le diaporama de soutenance oral `presentations/presentation-sprint1.md`.
- Synchroniser les versions dans `.sync/` et inviter le concepteur au commit.

#### Livrables
- Procès-verbal de Review : `sprints/pv-review-sprint1.md`.
- Fiche de Rétrospective : `sprints/retrospective-sprint1.md`.
- Diaporama de soutenance Marp complet : `presentations/presentation-sprint1.md`.
- Traçabilité miroir à jour dans `.sync/`.
