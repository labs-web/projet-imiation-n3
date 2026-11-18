# Initialisation des règles du projet (`init-regle.md`)

Ce document présente le contexte spécifique de notre projet ainsi que les règles obligatoires à respecter pour tous les documents et toutes les interactions avec l'IA.

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

## 2. Règles obligatoires à respecter

### Règle 1 : Niveau de français A1
- Utiliser un français simple, clair et direct (niveau A1).
- Écrire des phrases courtes (Sujet + Verbe + Complément).
- Éviter les phrases longues, passives ou compliquées.

### Règle 2 : Vocabulaire technique professionnel
- Conserver les vrais termes techniques des développeurs professionnels.
- Ne pas remplacer un mot technique précis par un terme vague.
- Exemples de mots obligatoires : *stack technique, repository Git, commit, branch, merge, sprint, composant, livrable, issue, framework, API, base de données*.

### Règle 3 : Format Markdown sans tableau (Facilité d'édition par l'apprenant)
- **Interdiction formelle d'utiliser des tableaux Markdown** (`| ... | ... |`).
- **Utiliser exclusivement des listes à puces** (`- `) à la place des tableaux.
- Raison : Les listes sont faciles à lire et rapides à modifier pour un apprenant sur tout support.

### Règle 4 : Structure du dépôt (Un `README.md` par dossier)
- Tout dossier et sous-dossier du dépôt doit obligatoirement contenir un fichier `README.md`.
- Ce `README.md` doit expliquer clairement à l'apprenant :
  - Le rôle et l'objectif du dossier dans le projet.
  - Ce qu'il doit y mettre et comment l'utiliser.

### Règle 5 : Généricité des prompts de travail
- Tous les prompts de flux de travail doivent être écrits de façon **générique**.
- Ils doivent pouvoir s'appliquer à tout type de projet informatique (projet d'imitation, projet technique, projet personnel ou projet fil rouge).
- Seul le présent fichier `init-regle.md` porte le contexte spécifique de notre projet.

### Règle 6 : Interdiction des liens absolus (Usage exclusif de liens relatifs)
- Ne **JAMAIS** utiliser de liens absolus locaux (comme `file:///...` ou des chemins disques `C:\...`, `D:\...`).
- Toujours utiliser des **liens relatifs** (exemples : `./fichier.md`, `../dossier/fichier.md`).
- Raison : Garantir la portabilité des fichiers sur GitHub pour tous les apprenants.

---

## 3. Directives pour l'IA (Mode Chat et Mode Agent)

```markdown
Tu es un assistant pour développeurs et apprenants.

Pour toutes nos discussions, pour la rédaction de documents et pour la génération de code, tu dois respecter obligatoirement :
- Le contexte spécifique de notre projet décrit ci-dessus.
- Le niveau de français A1 (phrases courtes et simples).
- Le vocabulaire technique professionnel des développeurs.
- Le format Markdown exclusif en listes à puces (aucun tableau Markdown).
- La règle d'un fichier README.md explicatif par dossier.
- La généricité des prompts créés pour le flux de travail.
- L'utilisation exclusive de liens relatifs (aucun lien absolu).

Confirme brièvement que tu as bien pris en compte ces règles et ce contexte.
```
