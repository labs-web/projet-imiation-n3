---
name: gestion-depot
description: >-
  Gère les opérations sur le dépôt Git/GitHub et le cycle de vie du projet.
  Charge et orchestre dynamiquement la mission requise dans son dossier missions/.
---

# Skill Gestion de Dépôt : /gestion-depot

## 1. Mission
Orchestrer la gouvernance et les opérations sur le dépôt Git/GitHub (initialisation, contrôle des branches de sprint, synchronisation et structuration).
Le skill délègue l'exécution à la mission spécialisée appropriée située dans son sous-dossier `missions/`.

## 2. Déclenchement
- **Quand l'activer** :
  - Sur appel direct `/gestion-depot [nom-mission]`.
  - Lors de l'étape 1 du flux de travail (`1. Création et initialisation du projet`).
  - Pour toute opération de configuration, contrôle de branche ou publication sur GitHub.
- **Quand NE PAS l'activer** :
  - Gestion du référentiel méthodologique (utiliser `flux-travail`).
  - Méta-gouvernance des compétences et règles (utiliser `skills-dev`).

## 3. Catalogue des missions du skill
Le skill dispose des missions unitaires suivantes dans `missions/` :
- `init-projet.md` : Initialisation Git locale, contrôle de la branche sprint active, publication GitHub et rédaction standardisée du `README.md` racine.

## 4. Protocole de routage et exécution dynamique
- **Étape 1 : Sélection de la mission** :
  - Si l'utilisateur mentionne une mission : sélectionner la mission correspondante dans `missions/`.
  - Si aucune mission n'est fournie : auditer l'état actuel du dépôt pour identifier la mission nécessaire.
- **Étape 2 : Chargement de la mission** :
  - Charger et lire le fichier `missions/<nom>.md` retenu.
- **Étape 3 : Exécution déléguée** :
  - Appliquer les tâches concrètes et le gabarit de livrable prescrits dans le fichier de mission chargé.

## 5. Règles obligatoires
- Français A1 et vocabulaire technique professionnel de développeur.
- Zéro tableau Markdown (utiliser exclusivement des listes à puces `- `).
- Liens relatifs exclusifs (`./`, `../`).
