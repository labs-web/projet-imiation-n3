# Créateur de Prompt (`prompt-creator.prompt.md`)

Créer un nouveau prompt d'étape compact et générique pour le flux de travail.

## Entrée
- Nom ou slug de l'étape.
- Tâches composant l'étape et livrables attendus.
- Règles ou outils spécifiques nécessaires.

## Structure standard du prompt généré
- `# [Titre de l'étape] ([numéro].[slug].prompt.md)`
- `## Tâches de l'étape` (liste ordonnée des tâches à accomplir)
- `## Livrables attendus` (livrables finaux validant l'étape)
- `## Protocole d'audit et exécution` :
  - Exécution directe sans plan si l'apprenant précise une tâche.
  - Audit des livrables et proposition d'un artefact plan si la demande est globale.
- `## Structure du livrable` (template ou plan standard si génération de document)
- `## Règles` (Français A1, termes techniques, listes sans tableaux, liens relatifs)

## Règles de conception du prompt
- **Séparation consigne / données** : Le prompt ne doit jamais contenir le travail à faire en dur ni de placeholder. Il définit le cadre de l'étape. Le travail à faire est apporté par l'apprenant ou déduit de la conversation par l'IA.
- **Compacité stricte** : Le prompt doit être le plus compact possible, uniquement pour expliquer la règle et la tâche à l'IA, sans texte superflu.
- **Généricité** : 100% générique (applicable à tout projet informatique).
- **Nommage** : Format `[numéro].[slug].prompt.md`.
- **Format Markdown** : Listes à puces uniquement (aucun tableau Markdown).
- **Liens relatifs** : Uniquement des liens relatifs (aucun lien absolu).
- **Indexation** : Rappeler d'ajouter le prompt dans `prompts/prompts-index.yml`.
