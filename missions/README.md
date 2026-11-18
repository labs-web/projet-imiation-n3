# Dossier des Missions (`missions/`)

Ce document explique à l'apprenant le rôle de ce dossier dans le projet et la méthode pour utiliser et créer des missions.

---

## 1. Rôle du dossier dans notre projet

Dans la méthode par imitation et la démarche d'ingénierie logicielle :
- Ce dossier regroupe toutes les **missions standardisées** nécessaires pour réaliser chaque étape du projet avec l'aide de l'Intelligence Artificielle.
- Il permet à l'apprenant de ne pas improviser : chaque étape de travail possède une mission précise avec des entrées claires, des règles de qualité et des livrables attendus.
- Il garantit l'homogénéité du code, des documents et de la méthodologie entre tous les apprenants.

---

## 2. Organisation du dossier

Ce dossier regroupe :
- Les missions d'initialisation pour cadrer les échanges avec l'IA.
- L'index YAML (`missions-index.yml`) qui référence l'ensemble des missions disponibles.
- Les missions d'étapes pour réaliser les travaux du flux de travail (`*.mission.md`).

---

## 3. Comment utiliser les missions ?

### Option A : Utilisation en mode Chat (ex. ChatGPT, Claude)
- Étape 1 : Copier et envoyer la mission d'initialisation générale (`init-ia.mission.md`) au début de la conversation.
- Étape 2 : Choisir dans [missions-index.yml](./missions-index.yml) la mission de l'étape à réaliser et l'envoyer avec vos données de travail.

### Option B : Utilisation en mode Agent (ex. Antigravity, Cursor)
- Étape 1 : L'agent charge `init-ia.mission.md` et `init-agent.mission.md`.
- Étape 2 : L'agent consulte automatiquement [missions-index.yml](./missions-index.yml) pour identifier la mission adaptée.
- Étape 3 : Valider la proposition de l'agent pour lancer l'exécution de l'étape.

---

## 4. Règles pour ajouter une nouvelle mission

Lorsque vous créez une nouvelle mission pour une nouvelle étape du flux de travail :
- **Séparation consigne / données** : la mission ne contient jamais le travail à faire en dur. Elle définit le cadre méthodologique. Le travail est fourni par l'apprenant ou déduit de la conversation.
- Nommer le fichier au format `[numéro].[slug].mission.md`.
- Écrire la mission de manière **générique** pour qu'elle soit réutilisable sur d'autres projets.
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- **Interdiction formelle des tableaux Markdown** : utiliser uniquement des listes à puces (`- `) pour que les apprenants puissent facilement modifier les livrables.
- **Interdiction des liens absolus** : utiliser exclusivement des liens relatifs.
- **Compacité stricte** : la mission doit être la plus compacte possible, uniquement pour expliquer la règle et la tâche à l'IA, sans texte superflu.
- Ajouter la nouvelle mission dans [missions-index.yml](./missions-index.yml) avec son `name` et sa `description`.
