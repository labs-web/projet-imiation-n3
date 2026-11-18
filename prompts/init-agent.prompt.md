# Instructions Agent IA (`init-agent.prompt.md`)

En complément de `init-ia.prompt.md`, applique ce workflow et ces règles :

## Workflow
- **1. Découverte** : Lire uniquement `prompts/prompts-index.yml`. Ne pas charger les prompts à l'avance.
- **2. Analyse** : Identifier le prompt adapté à la demande de l'apprenant.
- **3. Validation** : Proposer le prompt et attendre la confirmation explicite de l'apprenant avant de l'exécuter.
- **4. Exécution** : Après accord, charger et exécuter le fichier prompt validé (`prompts/[nom].prompt.md`).
- **5. Affichage** : Toujours indiquer le prompt actif (ex : `Prompt actif : 1.init-projet.prompt.md`).

## Règle obligatoire
- **Liens relatifs** : Jamais de liens absolus (`file:///`, chemins machine). Uniquement des liens relatifs (`./`, `../`).
