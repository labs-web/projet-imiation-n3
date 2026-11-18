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
  - `init-regle.md` : Contient le contexte du projet et les règles obligatoires de rédaction (Français A1, vocabulaire technique professionnel, zéro tableau Markdown, un `README.md` par dossier).
  - `init-agent.md` : Définit le protocole d'assistance pour un Agent IA autonome (analyse du besoin, proposition de prompt, attente de confirmation).
- **Catalogue des prompts** :
  - `prompts.md` : Liste descriptive de l'ensemble des prompts disponibles, lue par l'Agent IA.
- **Prompts par étape de travail** :
  - Fichiers nommés selon le format `[numéro].[slug].prompt.md` (exemple : `1.init-projet.prompt.md`).

---

## 3. Comment utiliser les prompts ?

### Option A : Utilisation en mode Chat (ex. ChatGPT, Claude)
- Étape 1 : Copier et envoyer le contenu de [init-regle.md](./init-regle.md) au début de la conversation.
- Étape 2 : Copier et envoyer le prompt correspondant à l'étape que vous souhaitez réaliser (ex : [1.init-projet.prompt.md](./1.init-projet.prompt.md)) avec vos données d'entrée.

### Option B : Utilisation en mode Agent (ex. Antigravity, Cursor)
- Étape 1 : L'agent charge [init-regle.md](./init-regle.md) et [init-agent.md](./init-agent.md).
- Étape 2 : L'agent consulte automatiquement [prompts.md](./prompts.md).
- Étape 3 : L'agent vous propose le prompt adapté et vous demande votre confirmation avant de travailler.

---

## 4. Règles pour ajouter un nouveau prompt

Lorsque vous créez un nouveau prompt pour une nouvelle étape du flux de travail :
- Nommer le fichier au format `[numéro].[slug].prompt.md`.
- Écrire le prompt de manière **générique** pour qu'il soit réutilisable sur d'autres projets.
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- **Interdiction formelle des tableaux Markdown** : utiliser uniquement des listes à puces (`- `) pour que les apprenants puissent facilement modifier les livrables.
- **Interdiction des liens absolus** : utiliser exclusivement des liens relatifs.
- Ajouter la description du nouveau prompt dans [prompts.md](./prompts.md).
