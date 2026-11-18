# Dossier des Prompts (`prompts/`)

Ce document explique à l'apprenant le rôle de ce dossier dans le projet et la méthode pour utiliser et créer des prompts.

---

## 1. Rôle du dossier dans notre projet

Dans la méthode par imitation et la démarche d'ingénierie logicielle :
- Ce dossier regroupe tous les **prompts standardisés** nécessaires pour réaliser chaque étape du projet avec l'aide de l'Intelligence Artificielle.
- Il permet à l'apprenant de ne pas improviser : chaque étape de travail possède un prompt précis avec des entrées claires, des règles de qualité et des livrables attendus.
- Il garantit l'homogénéité du code, des documents et de la méthodologie entre tous les apprenants.

---

## 2. Contenu du dossier

- **Fichiers d'initialisation** :
  - `init-ia.prompt.md` : Contient le contexte du projet et les règles générales obligatoires (Français A1, vocabulaire technique professionnel, zéro tableau Markdown, liens relatifs, un `README.md` par dossier).
  - `init-agent.prompt.md` : Définit le protocole d'assistance pour un Agent IA autonome (analyse du besoin, proposition de prompt, attente de confirmation, généricité et compacité).
- **Catalogue des prompts** :
  - `prompts-index.yml` : Index au format YAML contenant la liste des prompts (`name` et `description`), lu par l'Agent IA.
- **Prompts par étape de travail** :
  - Fichiers nommés selon le format `[numéro].[slug].prompt.md` (exemple : `1.init-projet.prompt.md`).

---

## 3. Comment utiliser les prompts ?

### Option A : Utilisation en mode Chat (ex. ChatGPT, Claude)
- Étape 1 : Copier et envoyer le contenu de [init-ia.prompt.md](./init-ia.prompt.md) au début de la conversation.
- Étape 2 : Copier et envoyer le prompt correspondant à l'étape que vous souhaitez réaliser (ex : [1.init-projet.prompt.md](./1.init-projet.prompt.md)) avec vos données d'entrée.

### Option B : Utilisation en mode Agent (ex. Antigravity, Cursor)
- Étape 1 : L'agent charge [init-ia.prompt.md](./init-ia.prompt.md) et [init-agent.prompt.md](./init-agent.prompt.md).
- Étape 2 : L'agent consulte automatiquement [prompts-index.yml](./prompts-index.yml).
- Étape 3 : L'agent vous propose le prompt adapté et vous demande votre confirmation avant de travailler.

---

## 4. Règles pour ajouter un nouveau prompt

Lorsque vous créez un nouveau prompt pour une nouvelle étape du flux de travail :
- Nommer le fichier au format `[numéro].[slug].prompt.md`.
- Écrire le prompt de manière **générique** pour qu'il soit réutilisable sur d'autres projets.
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- **Interdiction formelle des tableaux Markdown** : utiliser uniquement des listes à puces (`- `) pour que les apprenants puissent facilement modifier les livrables.
- **Interdiction des liens absolus** : utiliser exclusivement des liens relatifs.
- **Compacité stricte** : le prompt doit être le plus compact possible, uniquement pour expliquer la règle et la tâche à l'IA, sans texte superflu.
- Ajouter le nouveau prompt dans [prompts-index.yml](./prompts-index.yml) avec son `name` et sa `description`.
