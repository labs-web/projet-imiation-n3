# Référentiel des Méthodes d'Ingénierie Logicielle et d'Orchestration

Ce document présente les 4 méthodes fondatrices du développement logiciel et le cadre d'orchestration **Dual-Track Agile**.

---

## 1. Les 4 Méthodes de Référence

Le développement logiciel moderne s'appuie sur quatre démarches complémentaires :

### A. Design Thinking (DT) : Trouver le bon produit
- **Rôle** : Cette méthode place l'utilisateur au centre de la réflexion. Elle permet de concevoir une application utile, désirable et facile à prendre en main.
- **Phases de référence** :
  - **1. Empathie** : Observer les utilisateurs sur le terrain, mener des entretiens et comprendre leurs besoins réels.
  - **2. Définition** : Formuler clairement le problème central à résoudre et définir la proposition de valeur.
  - **3. Idéation** : Organiser des sessions de brainstorming pour explorer plusieurs pistes de solutions et fonctionnalités.
  - **4. Prototypage** : Créer l'UI Kit, modéliser le **User Flow** et dessiner les maquettes d'interface (wireframes et mockups).
  - **5. Test** : Mettre les maquettes entre les mains des utilisateurs pour tester l'ergonomie et recueillir leurs retours.

### B. Gestion de Projet (GP / Standard PMI) : Fixer et tenir le cadre
- **Rôle** : Cette démarche garantit la maîtrise des délais, du budget, du périmètre et de la qualité.
- **Phases de référence** :
  - **1. Initialisation** : Cadrer le projet, identifier les parties prenantes et valider l'opportunité.
  - **2. Planification** : Définir le planning, allouer les ressources et anticiper les risques.
  - **3. Exécution** : Coordonner l'équipe et piloter la production des livrables.
  - **4. Suivi et Maîtrise** : Contrôler l'avancement, valider la conformité et animer les comités de pilotage.
  - **5. Clôture** : Réceptionner officiellement le produit avec le client et dresser le bilan final.

### C. Processus de Développement Orienté Objet (Dev OO) : Construire le logiciel
- **Rôle** : Cette démarche assure la rigueur technique, la qualité du code et la pérennité de l'architecture.
- **Phases de référence** :
  - **1. Analyse** : Traduire les besoins utilisateurs en règles de gestion et cas d'utilisation précis.
  - **2. Conception** : Concevoir l'architecture logicielle (modèle 2 couches), les diagrammes de classes et la base de données.
  - **3. Implémentation** : Développer le code source (Laravel 12, Alpine.js, Tailwind CSS) en appliquant les bonnes pratiques.
  - **4. Tests et Validation** : Vérifier le fonctionnement par des tests unitaires, des tests d'intégration et la validation des critères d'acceptation.
  - **5. Déploiement et Maintenance** : Installer l'application sur le serveur de production et corriger les anomalies.

### D. Scrum : Organiser le rythme itératif
- **Rôle** : Ce cadre agile découpe le projet en cycles courts (Sprints) pour livrer rapidement de la valeur concrète.
- **Phases et rituels de référence** :
  - **1. Gestion du Product Backlog** : Rédiger, estimer et prioriser les User Stories en continu.
  - **2. Sprint Planning** : Sélectionner les User Stories prêtes et engager l'équipe sur le Sprint Goal.
  - **3. Daily Scrum** : Faire un point quotidien de 15 minutes pour synchroniser les équipiers et lever les blocages.
  - **4. Incrément et Definition of Done (DoD)** : Produire une version opérationnelle et testée du logiciel à chaque sprint.
  - **5. Sprint Review** : Démontrer l'incrément réalisé aux utilisateurs et adapter le Backlog.
  - **6. Sprint Retrospective** : Analyser le fonctionnement de l'équipe et décider d'actions d'amélioration.

---

## 2. Le Cadre d'Orchestration : Dual-Track Agile

Le cadre Dual-Track Agile synchronise la conception UX et le codage technique en faisant avancer deux pistes en parallèle :

- **Piste Discovery (Exploration & Maquettage)** :
  - L'équipe prépare les fonctionnalités du sprint suivant ($N+1$).
  - Elle clarifie les besoins, dessine le User Flow et réalise les maquettes en temps masqué (~10% du temps).
- **Piste Delivery (Développement & Livraison)** :
  - L'équipe développe et teste les fonctionnalités du sprint actif ($N$).
  - Elle s'engage uniquement sur des User Stories déjà validées et maquettées.

---

## 3. Définitions Méthodologiques Clés

### A. Le User Flow (Parcours Utilisateur)
- **Définition** : Le User Flow est un schéma visuel montrant le parcours complet qu'un utilisateur réalise écran par écran pour atteindre un but précis dans l'application.
- **Positionnement obligatoire** :
  - Le User Flow se place **entre l'Idéation et la réalisation des maquettes**.
  - L'Idéation détermine *quelles solutions* apporter.
  - Le User Flow détermine *comment l'utilisateur navigue* d'un écran à l'autre.
  - Les maquettes dessinent ensuite *à quoi ressemble chaque écran* du parcours.
- **Exemple** :
  `Page d'accueil -> Clic sur la carte d'un article -> Contrôleur vérifie l'identifiant -> Page détaillée de l'article affichée`.

### B. Le Persona
- Fiche synthétique représentant un utilisateur type avec ses motivations, ses compétences techniques et ses points de douleur.

### C. La User Story et le critère INVEST
- Description courte d'un besoin formulée ainsi : *« En tant que [rôle], je veux [action] afin de [bénéfice] »*.
- Une User Story doit respecter les critères INVEST : Indépendante, Négociable, Porteuse de Valeur, Estimable, Suffisamment petite (Sized appropriately) et Testable.

### D. La Definition of Ready (DoR) vs Definition of Done (DoD)
- **Definition of Ready (DoR)** : Critères qu'une User Story doit satisfaire pour entrer en développement (maquettes validées, critères d'acceptation clairs, règles de gestion définies).
- **Definition of Done (DoD)** : Critères de qualité qu'une fonctionnalité doit respecter pour être considérée terminée (code écrit, tests passants, gestion d'erreurs 404/500, zéro régression).

---

## 4. Matrice de Correspondance avec les 16 Étapes du Flux

Chaque étape du flux générique mobilise les phases de référence selon la logique suivante :

- **Étape 1 : Planifier le Sprint 0** -> Scrum (Sprint Planning 0) et Gestion de Projet (Initialisation).
- **Étape 2 : Cadrer le projet, choisir la stack et comprendre l'utilisateur** -> Gestion de Projet (Initialisation) et Design Thinking (Empathie).
- **Étape 3 : Définir la Vision Produit et le Product Backlog initial** -> Design Thinking (Définition & Idéation), Scrum (Backlog) et Dev OO (Analyse).
- **Étape 4 : Concevoir la Charte Graphique, le User Flow et les maquettes ciblées** -> Design Thinking (Prototypage) et Dev OO (Conception UI).
- **Étape 5 : Concevoir l'architecture et préparer le socle technique** -> Dev OO (Conception & Implémentation) et Gestion de Projet (Planification technique).
- **Étape 6 : Valider le socle, la charte graphique et les maquettes** -> Scrum (Sprint Review 0), Design Thinking (Test UX) et Gestion de Projet (Validation).
- **Étape 7 : Clôturer le Sprint 0** -> Scrum (Sprint Retrospective 0) et Gestion de Projet (Amélioration continue).
- **Étape 8 : Planifier le Sprint N** -> Scrum (Sprint Planning) et Gestion de Projet (Planification opérationnelle).
- **Étape 9 : Concevoir en détail et développer** -> Dev OO (Conception détaillée & Implémentation) et Gestion de Projet (Exécution).
- **Étape 10 : Affiner le Backlog et maquetter pour N+1** -> Design Thinking (Idéation & Prototypage) et Scrum (Backlog Refinement).
- **Étape 11 : Suivre l'avancement quotidien** -> Scrum (Daily Scrum) et Gestion de Projet (Suivi & Maîtrise).
- **Étape 12 : Tester et valider l'Incrément** -> Dev OO (Tests & Validation) et Scrum (Definition of Done).
- **Étape 13 : Présenter et inspecter** -> Scrum (Sprint Review), Design Thinking (Test UX) et Gestion de Projet (Recette).
- **Étape 14 : Améliorer le processus** -> Scrum (Sprint Retrospective) et Gestion de Projet (Amélioration continue).
- **Étape 15 : Déployer en production et valider en conditions réelles** -> Dev OO (Déploiement & Maintenance) et Gestion de Projet (Exécution finale).
- **Étape 16 : Clôturer officiellement le projet** -> Gestion de Projet (Clôture).
