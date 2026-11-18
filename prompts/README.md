# Dossier des Prompts (`prompts/`)

Ce document explique à l'apprenant le rôle de ce dossier dans le projet et la méthode pour utiliser et créer des prompts.

---

## 1. Rôle du dossier dans notre projet

Dans la méthode par imitation et la démarche d'ingénierie logicielle :
- Ce dossier regroupe tous les **prompts standardisés** nécessaires pour réaliser chaque étape du projet avec l'aide de l'Intelligence Artificielle.
- Il permet à l'apprenant de ne pas improviser : chaque étape de travail possède un prompt précis avec des entrées claires, des règles de qualité et des livrables attendus.
- Il garantit l'homogénéité du code, des documents et de la méthodologie entre tous les apprenants.

---

## 2. Organisation du dossier

Ce dossier regroupe :
- Les prompts d'initialisation pour cadrer les échanges avec l'IA.
- L'index YAML (`prompts-index.yml`) qui référence l'ensemble des prompts disponibles.
- Les prompts outillés pour réaliser les étapes du flux de travail.

---

## 3. Comment utiliser les prompts ?

### Option A : Utilisation en mode Chat (ex. ChatGPT, Claude)
- Étape 1 : Copier et envoyer le prompt d'initialisation générale (`init-ia.prompt.md`) au début de la conversation.
- Étape 2 : Choisir dans [prompts-index.yml](./prompts-index.yml) le prompt de l'étape à réaliser et l'envoyer avec vos données de travail.

### Option B : Utilisation en mode Agent (ex. Antigravity, Cursor)
- Étape 1 : L'agent charge `init-ia.prompt.md` et `init-agent.prompt.md`.
- Étape 2 : L'agent consulte automatiquement [prompts-index.yml](./prompts-index.yml) pour identifier le prompt adapté.
- Étape 3 : Valider la proposition de l'agent pour lancer l'exécution de l'étape.

---

## 4. Règles pour ajouter un nouveau prompt

Lorsque vous créez un nouveau prompt pour une nouvelle étape du flux de travail :
- **Séparation consigne / données** : le prompt ne contient jamais le travail à faire en dur. Il définit le cadre méthodologique. Le travail est fourni par l'apprenant ou déduit de la conversation.
- Nommer le fichier au format `[numéro].[slug].prompt.md`.
- Écrire le prompt de manière **générique** pour qu'il soit réutilisable sur d'autres projets.
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- **Interdiction formelle des tableaux Markdown** : utiliser uniquement des listes à puces (`- `) pour que les apprenants puissent facilement modifier les livrables.
- **Interdiction des liens absolus** : utiliser exclusivement des liens relatifs.
- **Compacité stricte** : le prompt doit être le plus compact possible, uniquement pour expliquer la règle et la tâche à l'IA, sans texte superflu.
- Ajouter le nouveau prompt dans [prompts-index.yml](./prompts-index.yml) avec son `name` et sa `description`.
