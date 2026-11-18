# Mission : Initialisation du Projet (`init-projet.md`)

Initialiser le projet en local, sécuriser la branche de sprint active, publier sur GitHub et structurer le fichier `README.md` racine.

## Tâches de la mission
- **Tâche 1 : Détection du sprint et contrôle de branche** : Identifier le sprint actif (ex: `sprint1`) et s'assurer que le travail est positionné sur la branche de sprint correspondante (`git checkout -b sprint1` ou `git checkout sprint1`).
- **Tâche 2 : Initialisation locale Git** : Vérifier ou exécuter l'initialisation Git locale (`git init`), configurer les exclusions (`.gitignore`) et réaliser le commit initial.
- **Tâche 3 : Publication sur GitHub** :
  - Publier le dépôt distant via GitHub CLI avec la commande : `gh repo create`.
  - Si GitHub CLI (`gh`) n'est pas installé ou non connecté : inviter l'apprenant à s'authentifier avec `gh auth login`.
- **Tâche 4 : Rédaction du README.md** : Reformuler et structurer le fichier `README.md` racine selon le gabarit des 6 sections ci-dessous en intégrant la stack technique du projet (Laravel 12).

## Livrables attendus
- Dépôt GitHub distant créé et synchronisé sur la branche de sprint active.
- Fichier `README.md` racine conforme aux standards Solicode.

## Protocole d'audit et exécution
- **Si l'apprenant précise une tâche** : Exécuter directement la tâche demandée sans créer d'artefact plan.
- **Si aucune tâche n'est précisée** : Auditer l'état des livrables (branche active, Git local, publication GitHub, contenu du `README.md`) et proposer les actions à réaliser dans un artefact plan pour validation.

## Structure du livrable (README.md)
- `# [Nom du Projet]`
- `## 1. Description du projet` (résumé en 2-3 phrases, utilisateurs cibles, déploiement)
- `## 2. Contexte et Objectifs` (contexte Solicode Tanger, formateur, objectifs techniques et pédagogiques)
- `## 3. Stack technique` (framework backend Laravel 12, frontend, base de données, Git)
- `## 4. Organisation des dossiers` (rôle des dossiers : `.agents/`, `docs/`, `flux-travail/`, `issues/`, `labs/`, `sprints/`)
- `## 5. Méthodologie` (Agile/Scrum, 2TUP, Design Thinking, modélisation UML)
- `## 6. Démarrage rapide` (prérequis, cloner, lancer)
