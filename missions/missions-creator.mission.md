# Créateur de Missions (`missions-creator.mission.md`)

Créer un nouveau fichier de mission compact et générique pour une étape du flux de travail.

## Entrée
- Nom ou slug de l'étape.
- Tâches composant l'étape et livrables attendus.
- Règles ou outils spécifiques nécessaires.

## Structure standard de la mission générée
- `# [Titre de l'étape] ([numéro].[slug].mission.md)`
- `## Tâches de la mission` (liste ordonnée des tâches à accomplir)
- `## Livrables attendus` (livrables finaux validant l'étape)
- `## Protocole d'audit et exécution` :
  - Exécution directe sans plan si l'apprenant précise une tâche.
  - Audit des livrables et proposition d'un artefact plan si la demande est globale.
- `## Structure du livrable` (template ou plan standard si génération de document)
- `## Règles spécifiques` (Optionnel : uniquement si contraintes propres à l'étape).

## Règles de conception de la mission
- **Séparation consigne / données** : La mission ne contient jamais le travail à faire en dur ni de placeholder. Le travail à faire est apporté par l'apprenant ou déduit de la conversation par l'IA.
- **Principe DRY et Héritage** : Ne jamais recopier les règles générales déjà formalisées dans `init-ia.mission.md` et `init-agent.mission.md`.
- **Compacité stricte** : Rédiger la mission de façon la plus concise possible, sans texte superflu.
- **Généricité** : 100% générique (applicable à tout projet informatique).
- **Nommage** : Format `[numéro].[slug].mission.md`.
- **Indexation** : Rappeler d'ajouter la mission dans `missions/missions-index.yml`.
