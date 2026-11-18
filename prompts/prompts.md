# Catalogue des Prompts du Projet (`prompts.md`)

Ce fichier recense tous les prompts disponibles dans le flux de travail. Il est lu par l'Agent IA pour identifier et proposer le prompt convenable selon la demande de l'apprenant.

---

## Prompts d'initialisation

- **Règles et contexte** : `init-regle.md`
  - Rôle : Définit le contexte du projet et les règles obligatoires (Français A1, vocabulaire technique professionnel, zéro tableau Markdown, un `README.md` par dossier).
  - Utilisation : Utilisé seul pour le mode Chat, et comme première étape pour le mode Agent.

- **Workflow de l'Agent IA** : `init-agent.md`
  - Rôle : Définit le protocole de l'agent (découverte via `prompts.md`, proposition de prompt, validation par l'apprenant, exécution).
  - Utilisation : Utilisé pour les agents autonomes outillés.

---

## Prompts des étapes de réalisation

- **Étape 1 - Initialisation du README** : `1.init-projet.prompt.md`
  - Slug : `init-projet`
  - Description : Nettoyer, reformuler et structurer le fichier `README.md` de description de projet à partir d'un texte brut ou brouillon.
  - Livrable généré : `README.md` (à la racine du dépôt).
