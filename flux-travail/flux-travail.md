# Flux de travail du projet

Ce document formalise les étapes de réalisation du Projet d'imitation Niveau 3. Il sert de référentiel méthodologique pour guider l'apprenant et l'Agent IA dans la production des livrables.

Les projets suivent les démarches d'ingénierie logicielle : 2TUP, Design Thinking, modélisation UML et méthodologie Agile/Scrum.

---

## Priorité 1. Création et initialisation du projet

### Prérequis
- Présentation du projet d'imitation par le formateur.
- Notions de base sur Git et GitHub.
  - Installation et utilisation de githuib CLI
  - Création des branche

### Travail à faire
- **Tâche 1 : Initialisation locale** : Créer le projet, initialiser Git (`git init`) et réaliser le premier commit.
- **Tâche 2 : Publication sur GitHub** :
  - Publier le dépôt via GitHub CLI avec la commande : `gh repo create`.
  - Si GitHub CLI n'est pas installé ou non connecté : Il faut informer l'apprenant de réaliser réaliser le lab `lab-github : installation et utilisation de github CLI`.
- **Tâche 3 : Rédaction du README.md** : Nettoyer et structurer le fichier `README.md` racine selon le template standard.

### Livrables
- Dépôt GitHub distant publié et accessible.
- Fichier `README.md` propre et conforme.
- Prompt d'étape : `prompts/1.init-projet.prompt.md`.

---

## Priorité 2. Initialisation de l'Agent IA

### Prérequis
- Réalisation du lab : Prompt-Engineering (formulation de consignes, rôles et règles IA).

### Travail à faire
- Définir le socle commun des règles et contexte du projet : `prompts/init-ia.prompt.md`.
- Définir le protocole de fonctionnement de l'Agent IA : `prompts/init-agent.prompt.md`.
- Créer la capacité de génération de prompts : `prompts/prompt-creator.prompt.md`.
- Mettre en place le catalogue des capacités : `prompts/prompts-index.yml`.
- Rédiger le guide d'utilisation du dossier : `prompts/README.md`.

### Livrables
- `prompts/init-ia.prompt.md`
- `prompts/init-agent.prompt.md`
- `prompts/prompt-creator.prompt.md`
- `prompts/prompts-index.yml`
- `prompts/README.md`

---

## Priorité 3. Documentation du Flux de Travail

### Prérequis
- Définition du flux de travail et de son rôle pour outiller l'Agent IA.

### Travail à faire
- Initialiser le document de suivi du flux de travail : `flux-travail/flux-travail.md`.
- Formaliser la structure standardisée des étapes (`Priorité`, `Prérequis`, `Travail à faire`, `Livrables`).
- Créer la capacité de gestion du flux : `prompts/flux-travail.prompt.md`.
- Rédiger le guide du dossier : `flux-travail/README.md`.

### Livrables
- Fichier `flux-travail/flux-travail.md`.
- Prompt d'étape : `prompts/flux-travail.prompt.md`.
- Guide pédagogique : `flux-travail/README.md`.

---

## Priorité 4. Création et Planification des issues

### Prérequis
- Méthodologie Agile/Scrum et planification de sprint.

### Travail à faire
- Créer l'espace de suivi des tâches du projet : dossier `issues/`.
- Recenser les tâches hors LMS ou demandées par le chef de projet.
- Organiser les issues par statut (`open`, `à-valider`, `closes`).
- Soumettre les issues à la validation du formateur avant dépôt sur GitHub.

### Livrables
- Guide pédagogique : `issues/README.md`.
- Fichiers de suivi des tâches : `issues/issues-open.md`, `issues/issues-à-valider.md`, `issues/issues-closes.md`.
