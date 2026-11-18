# Règles Générales de Rédaction et de Structure

Ces règles s'appliquent de manière générique à tous les fichiers et toutes les interactions de l'Agent IA.

---

## 1. Rédaction et langue

- **Niveau de français A1** :
  - Rédiger des phrases courtes, directes et simples (Sujet + Verbe + Complément).
  - Éviter les phrases longues, passives ou complexes.
- **Vocabulaire technique professionnel** :
  - Conserver les vrais termes techniques des développeurs professionnels.
  - Ne pas remplacer un mot technique précis par un terme vague.
  - Exemples de termes obligatoires : *stack technique, repository Git, commit, branch, merge, sprint, composant, livrable, issue, framework, API, base de données*.

---

## 2. Formatage Markdown

- **Format sans tableau (Facilité d'édition par l'apprenant)** :
  - Interdiction formelle d'utiliser des tableaux Markdown (`| ... | ... |`).
  - Utiliser exclusivement des listes à puces (`- `) à la place des tableaux.
  - Raison : Les listes sont faciles à lire et rapides à modifier pour un apprenant sur tout support.

---

## 3. Liens relatifs obligatoires

- **Interdiction formelle des liens absolus** :
  - Ne jamais écrire de chemins locaux (`C:\...`, `D:\...`) ou de liens de type `file:///...`.
  - Toujours utiliser des **liens relatifs** (exemples : `./fichier.md`, `../dossier/fichier.md`).
  - Raison : Garantir la portabilité des fichiers sur GitHub pour tous les utilisateurs.

---

## 4. Structure du dépôt

- **Un fichier `README.md` par dossier** :
  - Tout dossier et sous-dossier du dépôt doit obligatoirement contenir un fichier `README.md`.
  - Ce `README.md` doit expliquer clairement à l'apprenant :
    - Le rôle et l'objectif du dossier dans le projet.
    - Ce qu'il doit y mettre et comment l'utiliser.
