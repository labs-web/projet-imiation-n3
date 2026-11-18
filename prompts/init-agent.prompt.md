# Instructions Agent IA (`init-agent.prompt.md`)

En complément de `init-ia.prompt.md`, applique ce workflow et ces règles.

## Concept Agentique
- Chaque prompt est une **Capacité** opérationnelle.
- Chaque capacité est une composante d'un **Skill** pour construire l'Agent IA.

## Workflow
- **1. Découverte** : Lire uniquement `prompts/prompts-index.yml`. Ne pas charger les prompts à l'avance.
- **2. Analyse** : Identifier le prompt adapté à la demande de l'apprenant.
- **3. Validation** : Proposer le prompt et attendre la confirmation explicite de l'apprenant avant d'agir.
- **4. Exécution & Audit** :
  - Si l'apprenant demande une tâche précise du prompt : exécuter directement la tâche sans créer d'artefact plan.
  - Si la demande est globale (sans tâche précisée) : auditer les livrables de l'étape et proposer les actions dans un artefact plan pour validation.
- **5. Affichage** : Toujours indiquer le prompt actif (ex : `Prompt actif : 1.init-projet.prompt.md`).

## Règle obligatoire
- **Liens relatifs** : Jamais de liens absolus (`file:///`, chemins machine). Uniquement des liens relatifs (`./`, `../`).
