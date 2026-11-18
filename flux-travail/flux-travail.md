# Flux de travail du projet

Ce document formalise les étapes de réalisation du Projet d'imitation Niveau 3. Il sert de référentiel méthodologique pour guider l'apprenant (mode Chatbot) et l'Agent IA (mode Agent outillé) dans la production des livrables.

Les projets suivent les démarches d'ingénierie logicielle : 2TUP, Design Thinking, modélisation UML et méthodologie Agile/Scrum.

La planification des sprints et l'identification du sprint actif sont centralisées dans [sprints/sprints.md](../sprints/sprints.md).

---

# Sprint 1 : Initialisation et Cadrage

Ce premier sprint regroupe les étapes fondatrices du projet. Il permet de mettre en place le dépôt, d'outiller l'Agent IA et de formaliser le cadre méthodologique.

---

## 1. Création et initialisation du projet

### Base théorique et pratique
- `lab-github` : Installation et utilisation de GitHub CLI (`gh repo create`).
- `lab-git` : Création et gestion des branches Git (`sprint[N]`).

### Prérequis
- Présentation du projet d'imitation par le formateur.
- Notions de base sur Git et GitHub.

### Travail à faire
- **Tâche 1 : Initialisation locale** : Créer le projet, initialiser Git (`git init`) et réaliser le premier commit.
- **Tâche 2 : Publication sur GitHub** : Créer la branche `sprint1` et publier le dépôt via GitHub CLI avec la commande : `gh repo create`.
- **Tâche 3 : Rédaction du README.md** : Nettoyer et structurer le fichier `README.md` racine selon le template standard Solicode en intégrant la stack technique (Laravel).

### Livrables
- Dépôt GitHub distant publié et synchronisé sur la branche `sprint1`.
- Fichier `README.md` propre et conforme.
- Planification Scrum : `sprints/sprints.md` et `sprints/README.md`.
- Skill outillé (mode agent) : `.agents/skills/gestion-depot/SKILL.md`.
- Mission d'étape (mode chatbot) : `missions/1.init-projet.mission.md`.

---

## 2. Initialisation de l'Agent IA

### Base théorique et pratique
- `lab-prompt-engineering` : Formulation de consignes, rôles et règles IA.
- `lab-agent-ia` : Architecture d'un agent outillé (règles et skills).

### Prérequis
- Dépôt Git initialisé et publié sur GitHub sur la branche `sprint1` (Étape 1).

### Travail à faire
- Définir le socle commun des règles et contexte du projet : `.agents/rules/contexte-projet.md`, `.agents/rules/regles-generales.md` et `missions/init-ia.mission.md`.
- Définir le protocole de fonctionnement de l'Agent IA : `missions/init-agent.mission.md`.
- Mettre en place les skills initiaux dans `.agents/skills/` (`skills-dev`, `missions-creator`, `gestion-depot`, `marp`, `realisation-ua-lab`).
- Mettre en place le catalogue des missions : `missions/missions-index.yml`.
- Rédiger le guide d'utilisation du dossier : `missions/README.md`.

### Livrables
- Règles permanentes : `.agents/rules/contexte-projet.md`, `.agents/rules/regles-generales.md`.
- Skills agentiques configurés dans `.agents/skills/`.
- Missions d'initialisation : `missions/init-ia.mission.md`, `missions/init-agent.mission.md`, `missions/missions-creator.mission.md`, `missions/missions-index.yml`, `missions/README.md`.

---

## 3. Documentation du Flux de Travail

### Base théorique et pratique
- `lab-flux-travail` : Démarche 2TUP, ingénierie logicielle et formalisation des étapes.

### Prérequis
- Initialisation de l'Agent IA terminée (Étape 2).

### Travail à faire
- Initialiser le document de suivi du flux de travail : `flux-travail/flux-travail.md`.
- Formaliser la structure standardisée des étapes (`Base théorique et pratique`, `Prérequis`, `Travail à faire`, `Livrables`).
- Créer la mission de gestion du flux : `missions/flux-travail.mission.md`.
- Rédiger le guide du dossier : `flux-travail/README.md`.

### Livrables
- Fichier `flux-travail/flux-travail.md`.
- Mission d'étape : `missions/flux-travail.mission.md`.
- Guide pédagogique : `flux-travail/README.md`.

---

# Cycle de développement récurrent (Répété à chaque Sprint)

Les étapes suivantes constituent la boucle Scrum récurrente. Elles sont reproduites à chaque itération (Sprint 1, Sprint 2, etc.) en fonction des objectifs fixés dans `sprints/sprints.md`.

---

## 4. Création et Planification des issues

### Base théorique et pratique
- `lab-scrum-planning` : Méthodologie Agile/Scrum, découpage en user stories et planification de sprint.

### Prérequis
- Documentation du flux de travail initialisée (Étape 3).
- Fichier de planification des sprints initialisé (`sprints/sprints.md`).

### Travail à faire
- Créer l'espace de suivi des tâches du projet : dossier `issues/`.
- Recenser les tâches hors LMS ou demandées par le chef de projet pour le sprint actif.
- Organiser les issues par statut (`open`, `à-valider`, `closes`).
- Soumettre les issues à la validation du formateur avant dépôt sur GitHub.

### Livrables
- Guide pédagogique : `issues/README.md`.
- Fichiers de suivi des tâches : `issues/issues-open.md`, `issues/issues-à-valider.md`, `issues/issues-closes.md`.
