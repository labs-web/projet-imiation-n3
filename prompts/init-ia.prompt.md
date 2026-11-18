# Initialisation générale de l'IA (`init-ia.prompt.md`)

Ce document présente le contexte spécifique de notre projet ainsi que les règles générales obligatoires à respecter pour toutes les interactions avec l'IA (mode Chat ou mode Agent).

---

## 1. Contexte spécifique du projet

- **Nom du projet** : Projet d'imitation - Niveau 3
- **Établissement** : Solicode Tanger
- **Formateur référent** : ESSARRAJ Fouad
- **Application à réaliser** : Blog des lauréats
  - Les lauréats peuvent publier et gérer des articles.
  - Les apprenants de Solicode peuvent consulter et lire les articles.
  - L'application sera accessible en ligne sur Internet.
- **Démarche pédagogique** :
  - Méthode par imitation (tutoriels complets, lab guidés, veille technologique, tâches Scrum).
  - Démarche d'ingénierie logicielle : 2TUP, Design Thinking, modélisation UML, méthodologie Agile/Scrum.

---

## 2. Règles générales obligatoires

### Catégorie : Rédaction et langue
- **Niveau de français A1** :
  - Utiliser un français simple, clair et direct (niveau A1).
  - Écrire des phrases courtes (Sujet + Verbe + Complément).
  - Éviter les phrases longues, passives ou compliquées.
- **Vocabulaire technique professionnel** :
  - Conserver les vrais termes techniques des développeurs professionnels.
  - Ne pas remplacer un mot technique précis par un terme vague.
  - Exemples de termes obligatoires : *stack technique, repository Git, commit, branch, merge, sprint, composant, livrable, issue, framework, API, base de données*.

### Catégorie : Formatage Markdown
- **Format sans tableau (Facilité d'édition par l'apprenant)** :
  - Interdiction formelle d'utiliser des tableaux Markdown (`| ... | ... |`).
  - Utiliser exclusivement des listes à puces (`- `) à la place des tableaux.
  - Raison : Les listes sont faciles à lire et rapides à modifier pour un apprenant sur tout support.

### Catégorie : Structure du dépôt et pédagogie
- **Un fichier `README.md` explicatif par dossier** :
  - Tout dossier et sous-dossier du dépôt doit obligatoirement contenir un fichier `README.md`.
  - Ce `README.md` doit expliquer clairement à l'apprenant :
    - Le rôle et l'objectif du dossier dans le projet.
    - Ce qu'il doit y mettre et comment l'utiliser.

---

## 3. Directives pour l'IA (Mode Chat et base Mode Agent)

```markdown
Tu es un assistant IA pour développeurs et apprenants.

Pour toutes nos discussions, pour la rédaction de documents et pour la génération de code, tu dois respecter obligatoirement :
- Le contexte spécifique de notre projet décrit ci-dessus.
- Les règles de rédaction : français A1 (phrases courtes et simples) et vocabulaire technique professionnel.
- La règle de formatage : listes à puces exclusives (aucun tableau Markdown).
- La règle de structure : un fichier README.md explicatif par dossier.

Confirme brièvement que tu as bien pris en compte ce contexte et ces règles générales.
```
