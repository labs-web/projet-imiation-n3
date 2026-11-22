# Mission : Initialisation du Dépôt Git & Arborescence (`initialiser-depot-git.md`)

## 1. Contexte & Rôle
Cette mission pose les fondations physiques de configuration Git et de structure de dossiers pour tout projet web applicatif. Elle garantit un espace de travail standardisé, propre et sécurisé avant tout développement.

---

## 2. Procédure Pas-à-Pas

1. **Contrôle et Configuration Git :**
   - Vérifier l'initialisation du dépôt Git local (`git status`).
   - Vérifier la configuration de la branche active du sprint (`sprint0` ou branche de travail en cours).
   - Vérifier la liaison avec le dépôt distant distant (remote `origin`).

2. **Mise en Place du `.gitignore` Standardisé :**
   - Configurer les exclusions indispensables selon la stack technique (ex: Laravel, Composer, Node) :
     - Environnements et secrets : `.env`, `.env.backup`, `.env.production`.
     - Dépendances logicielles : `/vendor`, `/node_modules`.
     - Caches et compilations : `/storage/*.key`, `/storage/framework/`, `/public/build/`, `/public/hot`.
     - Outils de développement et IDE : `.idea`, `.vscode/*.json` (sauf configurations partagées), `.phpunit.result.cache`.

3. **Vérification et Création de l'Arborescence Projet Standardisée :**
   - Contrôler l'existence des répertoires professionnels du projet :
     - `docs/` : Documentation d'ingénierie (`cadrage/`, `analyse/`, `produit/`, `conception/`, `architecture/`, `qualite/`, `deploiement/`).
     - `sprints/` : Feuilles d'engagement de sprint, procès-verbaux de revues et rétrospectives.
     - `scrum/` : Product Backlog vivant et priorisé.
     - `src/` : Code source applicatif du projet.

4. **Vérification Finale :**
   - Exécuter `git status` pour contrôler les fichiers suivis et non suivis.
   - Présenter l'état à l'utilisateur et l'inviter à valider.
