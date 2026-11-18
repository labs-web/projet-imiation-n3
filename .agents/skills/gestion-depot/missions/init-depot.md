# Mission : Initialisation du Dépôt (`init-depot.md`)

Initialiser le dépôt Git local, contrôler la branche active du sprint et publier le projet sur GitHub.

## Tâches de la mission
- **Tâche 1 : Détection du sprint et contrôle de branche** : Identifier le sprint actif dans `sprints/sprints.md` (ex: `sprint1`) et s'assurer que le travail est positionné sur la branche de sprint correspondante (`git checkout -b sprint1` ou `git checkout sprint1`).
- **Tâche 2 : Initialisation locale Git** : Vérifier ou exécuter l'initialisation Git locale (`git init`), configurer les exclusions (`.gitignore`) et réaliser le commit initial.
- **Tâche 3 : Publication sur GitHub** :
  - Publier le dépôt distant via GitHub CLI avec la commande : `gh repo create`.
  - Si GitHub CLI (`gh`) n'est pas installé ou non connecté : inviter l'apprenant à s'authentifier avec `gh auth login`.
  - Pousser la branche de travail active : `git push -u origin sprint1`.

## Livrables attendus
- Dépôt GitHub distant créé et synchronisé sur la branche de sprint active (`sprint1`).
- Historique Git initialisé proprement avec la branche de travail.

## Protocole d'audit et exécution
- **Si l'apprenant précise une tâche** : Exécuter directement la tâche demandée sans créer d'artefact plan.
- **Si aucune tâche n'est précisée** : Auditer l'état du dépôt (branche active, statut Git local, synchronisation GitHub) et proposer les actions à réaliser dans un artefact plan pour validation.
