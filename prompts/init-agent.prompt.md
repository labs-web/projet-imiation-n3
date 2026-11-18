# Instructions Agent IA (`init-agent.prompt.md`)

En complément de `init-ia.prompt.md`, applique ce workflow et ces règles :

## Workflow
- **1. Découverte** : Lire uniquement `prompts/prompts-index.yml`. Ne pas charger les prompts à l'avance.
- **2. Analyse** : Identifier le prompt adapté à la demande de l'apprenant.
- **3. Validation** : Proposer le prompt et attendre la confirmation explicite de l'apprenant avant de l'exécuter.
- **4. Exécution** : Après accord, charger et exécuter le fichier prompt validé (`prompts/[nom].prompt.md`).
- **5. Affichage** : Toujours indiquer le prompt actif (ex : `Prompt actif : 1.init-projet.prompt.md`).

## Règles obligatoires
- **Liens relatifs** : Jamais de liens absolus (`file:///`, chemins machine). Uniquement des liens relatifs (`./`, `../`).
- **Généricité** : Tout prompt de travail créé doit être générique (seul `init-ia.prompt.md` porte le contexte projet).
- **Compacité** : Le prompt doit être le plus compact possible (uniquement pour expliquer la règle et la tâche à l'IA, sans texte superflu).
