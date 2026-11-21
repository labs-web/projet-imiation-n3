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

- **Un fichier `README.md` par dossier structurel racine** :
  - Les dossiers structurels du dépôt (`docs/`, `sprints/`, `scrum/`, `rapport/`, `presentations/`, `tutoriels/`) contiennent un fichier `README.md` expliquant le rôle du dossier.
  - **Exception stricte pour `tutoriels/` :** Uniquement `tutoriels/README.md`. Interdiction formelle d'ajouter des fichiers `README.md` dans les sous-dossiers de domaines, d'UAs ou de tutoriels unitaires (se référer à `.agents/references/gestion-livrables.md`).

---

## 5. Gestion des Sprints et branches Git

- **Conformité GitFlow et Souveraineté de l'Apprenant** :
  - Se référer impérativement à `.agents/references/gitflow.md`.
  - **Interdiction formelle de commit et push par l'Agent IA** : L'Agent IA ne doit jamais exécuter les commandes `git commit` ou `git push`.
  - Seul l'apprenant réalise les commits et les pushs sur son dépôt.
  - L'Agent IA modifie et crée les fichiers demandés, vérifie leur conformité (`git status`), et invite l'apprenant à valider et committer.
- **Interdiction de travailler directement sur `main`** :
  - Tout travail de développement, de documentation ou de sprint doit s'effectuer sur la branche dédiée au sprint actif (`sprint[N]`).
- **Détection du sprint actif** :
  - L'Agent IA consulte `sprints/sprints.md` pour identifier le sprint ayant le statut **Actif**.
  - L'Agent IA vérifie sa branche Git (`git branch --show-current`) et bascule sur la branche correspondante (`git checkout -b sprint[N]`).

---

## 6. Références Normatives Centralisées

Tout agent opérant dans ce dépôt (notamment l'**Agent Réalisation de Sprint**) applique obligatoirement le socle normatif :
- Identité et posture : `.agents/rules/persona.md`
- Cartographie physique des livrables : `.agents/references/gestion-livrables.md`
- Typologie et slugs des tutoriels : `.agents/references/typologie-uas-tutoriels.md`
- Stratégie des branches et conventions de commits : `.agents/references/gitflow.md`

---

## 6. Gouvernance des Flux de Travail et des Sessions

- **Référentiel universel vs Déclinaisons pédagogiques** :
  - Le flux générique d'ingénierie logicielle (`flux-travail/flux-travail-generique.md` - 25 étapes) est gouverné par le skill `flux-travail`.
  - La conception, le découpage et l'audit des flux opérationnels de formation (`flux-travail/sessions/`) sont gouvernés par le skill `conception-session`.
  - Consulter obligatoirement le document de gouvernance : [regles-flux-sessions.md](./regles-flux-sessions.md).
