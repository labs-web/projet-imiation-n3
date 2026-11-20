---
name: flux-travail
description: >-
  Gère, insère et audite les étapes de réalisation dans flux-travail/ (flux générique
  d'ingénierie logicielle et flux opérationnels par session dans sessions/) selon la structure normalisée.
---

# Skill Flux de Travail : /flux-travail

## 1. Mission
Piloter la structure, l'insertion et l'audit des étapes dans l'espace `flux-travail/` selon la démarche d'ingénierie logicielle unifiée (Design Thinking, Gestion de Projet PMI, Processus OO et Scrum Dual-Track).

Le skill maintient le découpage rigoureux entre :
1. **Le flux générique d'ingénierie logicielle** (`flux-travail/flux-travail-generique.md`) : Processus universel en 25 étapes réparties en 3 phases (Sprint 0 Cadrage & Socle, Cycle Dual-Track Sprint $N$ avec pistes Discovery et Delivery, Livraison et Clôture).
2. **Les flux opérationnels par session** (`flux-travail/sessions/`) : Découpage par session de formation N3 (S0 à S8) alternant directement les unités d'apprentissage (**UA-labs**) avec les étapes de réalisation concrètes.

## 2. Déclenchement
- **Quand l'activer** :
  - Ajout, reformulation ou audit d'une étape d'ingénierie logicielle dans `flux-travail/flux-travail-generique.md`.
  - Insertion, mise à jour ou audit d'un flux de session dans `flux-travail/sessions/` (`flux-travail-s0.md` à `flux-travail-s8.md`).
  - Évolution des guides méthodologiques dans `flux-travail/docs/`.
- **Quand NE PAS l'activer** :
  - Réalisation technique d'une fonctionnalité de code (utiliser le skill métier dédié).
  - Cérémonies de fin de sprint (utiliser `cloture-sprint`).
  - Production autonome de tutoriels d'autoformation (utiliser `realisation-ua-lab`).

## 3. Structure d'une Session de Formation (`flux-travail/sessions/`)
Chaque session de formation respecte les principes suivants :
- **Identification & Objectif :** Fiche d'identification, durée ferme (80h) et objectif d'apprentissage global.
- **Cadre Tri-Projets :** Projet d'Imitation (J1-7), Projet Technique en codage pur sans conception (J8), Projet Fil Rouge avec création de Skills agentiques (J9-10).
- **Intercalage Synchrone :** Chaque UA-lab est positionné immédiatement avant son utilisation pratique en réalisation.
- **Un seul UA-lab par domaine mobilisé :** Unité consolidée désignée par `UA-lab : [Titre] (Domaine D.xxx.x)` sans code numérique `UA.*`.
- **Noms Génériques Stricts :** Les étapes de réalisation reprennent les intitulés exacts du flux générique et livrent un seul livrable principal unique.

## 4. Règles Obligatoires
- Français niveau A1 direct et vocabulaire professionnel de développeur.
- **Interdiction formelle de tout tableau Markdown** (`| ... |`) : utiliser exclusivement des listes à puces directes (`- `).
- Liens relatifs exclusifs (`./`, `../`).
- Respect strict de la stack technique : **Laravel 13**, **MySQL exclusivement**, **Tailwind CSS avec Preline UI**, **Alpine.js**, **Agent Antigravity & GitHub Copilot**, et **Policies/Gates + Spatie (RBAC)**.
