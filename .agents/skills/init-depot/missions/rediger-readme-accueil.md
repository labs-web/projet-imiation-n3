# Mission : Rédaction du README Vitrine d'Accueil (`rediger-readme-accueil.md`)

## 1. Contexte & Rôle
Cette mission produit le document d'accueil vitrine `README.md` à la racine de tout projet web applicatif. Elle fournit aux développeurs, aux parties prenantes et aux évaluateurs une vision synthétique du projet, de son architecture et les instructions de prise en main immédiate.

---

## 2. Structure Normative du `README.md`

Le document est structuré de façon professionnelle sans aucun tableau Markdown :

1. **En-tête & Identité du Projet :**
   - Titre du projet : nom officiel de l'application (extrait du contexte projet ou fourni par le concepteur).
   - Présentation synthétique : résumé clair de la proposition de valeur, des objectifs métier et du public cible.
   - Équipe & Gouvernance : auteurs, cadre de réalisation et rôles clés.

2. **Architecture & Stack Technique de Référence :**
   - Backend : Framework serveur et langage (ex: Laravel 13 / PHP).
   - Base de données : Système de persistance (ex: MySQL).
   - Interface : Framework CSS et bibliothèque de composants (ex: Tailwind CSS & Preline UI).
   - Frontend réactif : Bibliothèque légère de réactivité client (ex: Alpine.js).
   - Sécurité : Gestion des rôles, permissions et politiques d'accès.
   - Outils de développement et automatisation.

3. **Organisation des Dossiers du Dépôt :**
   - `docs/` : Dossiers d'ingénierie (cadrage, analyse, conception, architecture, qualité).
   - `sprints/` : Suivi agile des sprints, feuilles de route et rétrospectives.
   - `scrum/` : Product Backlog ordonné.
   - `src/` : Code source applicatif de la solution.

4. **Guide d'Installation et de Démarrage Rapide :**
   - Prérequis logiciels (PHP, Composer, Node.js, SGBD).
   - Commandes pas-à-pas :
     - Clonage du dépôt.
     - Installation des dépendances backend (`composer install`) et frontend (`npm install`).
     - Configuration du fichier d'environnement (`cp .env.example .env` et `php artisan key:generate`).
     - Exécution des migrations et seeders (`php artisan migrate`).
     - Lancement des serveurs de développement.

5. **Gouvernance Git & Cycle de Contribution :**
   - Rappel de la convention de branches (`sprint[N]`, `feature/...`).
   - Engagement de validation et commits atomiques sous la responsabilité humaine.
