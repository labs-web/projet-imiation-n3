---
name: gestion-depot
description: >-
  Gère les opérations sur le dépôt Git/GitHub et le cycle de vie du projet.
  Sélectionne et exécute la mission appropriée dans son dossier missions/.
---

# Skill Gestion de Dépôt : /gestion-depot

## 1. Mission
Gérer les opérations sur le dépôt Git/GitHub (initialisation locale, gestion des branches de sprint, synchronisation distante et documentation racine).

## 2. Déclenchement
- **Quand l'activer** :
  - Le concepteur demande un travail sur le dépôt (initialiser Git, publier sur GitHub, changer de branche, mettre à jour le README racine, créer l'arborescence de présentations et rapport).
  - Exécution de l'étape 1 du flux de travail (`1. Création et initialisation du projet`).
- **Quand NE PAS l'activer** :
  - Évolution du flux de travail (utiliser `flux-travail`).
  - Création ou modification de skills (utiliser `skills-dev`).

## 3. Missions disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- `missions/init-depot.md` : Initialiser Git en local, basculer sur la branche active du sprint et publier sur GitHub avec GitHub CLI.
- `missions/init-projet.md` : Structurer le `README.md` racine et initialiser les dossiers de documentation (`presentations/` et `rapport/` avec script Node.js).
