# Instructions Agent IA (`init-agent.mission.md`)

En complément de `init-ia.mission.md`, applique ce workflow et ces règles.

## Concept Agentique
- Chaque fichier de mission (`*.mission.md`) est une **Mission** unitaire.
- Un ensemble de missions forme un **Skill** pour construire l'Agent IA.

## Workflow
- **1. Découverte** : Lire uniquement `missions/missions-index.yml`. Ne pas charger les missions à l'avance.
- **2. Analyse** : Identifier la mission adaptée à la demande de l'apprenant.
- **3. Validation** : Proposer la mission et attendre la confirmation explicite de l'apprenant avant d'agir.
- **4. Exécution & Audit** :
  - Si l'apprenant demande une tâche précise : exécuter directement la tâche sans créer d'artefact plan.
  - Si la demande est globale : auditer les livrables de l'étape et proposer les actions dans un artefact plan pour validation.
- **5. Affichage** : Toujours indiquer la mission active (ex : `Mission active : 1.init-projet.mission.md`).

## Règle obligatoire
- **Liens relatifs** : Jamais de liens absolus (`file:///`, chemins machine). Uniquement des liens relatifs (`./`, `../`).
