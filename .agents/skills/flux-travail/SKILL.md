---
name: flux-travail
description: >-
  Gouverne le flux générique d'ingénierie logicielle (25 étapes universelles)
  et la structure d'ensemble du répertoire flux-travail/.
---

# Skill Flux de Travail : /flux-travail

## 1. Mission
Gouverner, faire évoluer et auditer le **flux générique d'ingénierie logicielle** (`flux-travail/flux-travail-generique.md` - 25 étapes universelles) et l'intégrité de l'espace documentaire `flux-travail/`.
Le skill garantit la cohérence du processus unifié : Design Thinking, Gestion de Projet PMI, Processus OO et Scrum Dual-Track.

## 2. Déclenchement
- **Quand l'activer** :
  - Ajout, reformulation ou audit d'une étape universelle dans `flux-travail/flux-travail-generique.md`.
  - Évolution des guides méthodologiques transversaux dans `flux-travail/docs/`.
  - Contrôle d'alignement architectural global du projet.
- **Quand NE PAS l'activer** :
  - Conception, découpage ou mise à jour des flux de sessions de formation (`flux-travail/sessions/`) -> déléguer au skill `conception-session`.
  - Réalisation technique d'une fonctionnalité de code -> utiliser le skill métier dédié.
  - Cérémonies de fin de sprint -> utiliser `cloture-sprint`.
  - Production des tutoriels d'autoformation -> utiliser `realisation-ua-lab`.

## 3. Gouvernance et Interface avec `conception-session`
- Le skill `flux-travail` détient l'autorité exclusive sur les 25 étapes du flux universel.
- Les flux de sessions de formation (`flux-travail/sessions/`) sont conçus et gouvernés par le skill `conception-session` selon le document [regles-flux-sessions.md](../../rules/regles-flux-sessions.md).
- Toute demande d'évolution d'un intitulé générique émise lors de la conception d'une session doit être instruite et arbitrée par `flux-travail`.

## 4. Règles Obligatoires
- Français niveau A1 direct et vocabulaire professionnel de développeur.
- Interdiction formelle de tout tableau Markdown (`| ... |`) : listes à puces directes (`- `) exclusives.
- Liens relatifs obligatoires (`./`, `../`).
- Stack technique de référence : Laravel 13, MySQL, Tailwind CSS avec Preline UI, Alpine.js.
