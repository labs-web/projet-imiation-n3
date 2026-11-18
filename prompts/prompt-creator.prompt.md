# Créateur de Prompt (`prompt-creator.prompt.md`)

Créer un nouveau prompt compact et générique pour une étape du flux de travail.

## Entrée
- Nom ou slug de l'étape.
- Objectif de l'étape et livrables attendus.
- Données d'entrée (input) et consignes spécifiques.

## Structure attendue du prompt généré
- `# [Titre de l'étape] ([numéro].[slug].prompt.md)`
- `## Entrée` (données attendues pour cette étape)
- `## Sortie` (structure du livrable attendu)
- `## Règles` (consignes d'exécution spécifiques)
- `---`
- `### Données à traiter :`
- `[COLLER ICI LES DONNÉES]`

## Règles de conception du prompt
- **Compacité stricte** : Le prompt doit être le plus compact possible, uniquement pour expliquer la règle et la consigne à l'IA, sans texte superflu.
- **Généricité** : 100% générique (applicable à tout projet informatique).
- **Nommage** : Format `[numéro].[slug].prompt.md`.
- **Format Markdown** : Listes à puces uniquement (aucun tableau Markdown).
- **Liens relatifs** : Uniquement des liens relatifs (aucun lien absolu).
- **Indexation** : Rappeler d'ajouter le prompt dans `prompts/prompts-index.yml`.

---
### Informations de l'étape à traiter :
[COLLER ICI LES INFORMATIONS DE L'ÉTAPE]
