---
name: flux-travail
description: >-
  Gère, insère et audite les étapes de réalisation dans flux-travail/ (flux générique
  d'ingénierie logicielle et flux pédagogique de formation) selon la structure normalisée.
---

# Skill Flux de Travail : /flux-travail

## 1. Mission
Piloter la structure, l'insertion et l'audit des étapes dans l'espace `flux-travail/` selon la démarche d'ingénierie logicielle unifiée (Design Thinking, Gestion de Projet PMI, Processus OO et Scrum Dual-Track).

Le skill maintient le découpage rigoureux entre :
1. **Le flux générique d'ingénierie logicielle** (`flux-travail/flux-travail-generique.md`) : Processus universel en 16 étapes (Sprint 0, Cycle Dual-Track Sprint $N$ avec pistes Discovery et Delivery, Livraison et Clôture).
2. **Le flux pédagogique de formation** (`flux-travail/flux-travail-pedagogique.md`) : Découpage par session de formation structuré selon la norme à 4 sections.

## 2. Déclenchement
- **Quand l'activer** :
  - Ajout, reformulation ou audit d'une étape d'ingénierie logicielle dans `flux-travail/flux-travail-generique.md`.
  - Insertion ou mise à jour d'une étape de formation dans `flux-travail/flux-travail-pedagogique.md`.
  - Évolution des guides méthodologiques dans `flux-travail/docs/`.
- **Quand NE PAS l'activer** :
  - Réalisation technique d'une fonctionnalité de code (utiliser le skill métier dédié).
  - Cérémonies de fin de sprint (utiliser `cloture-sprint`).
  - Production autonome de livrables d'ateliers (utiliser `realisation-ua-lab`).

## 3. Structure d'une Étape Pédagogique (Format Standard à 4 Sections)
Chaque étape insérée dans `flux-travail-pedagogique.md` doit obligatoirement respecter l'ordre suivant :
- `## Étape [N] : [Titre de l'étape]` (référence vers l'étape générique correspondante)
- `### Base théorique et pratique` (codes officiels `UA.*`, liens vers tutoriels de référence)
- `### Prérequis` (validations préalables, livrables d'étapes antérieures)
- `### Travail à faire` (tâches opérationnelles ordonnées)
- `### Livrables` (fichiers physiques produits et versions dans `.sync/`)

## 4. Règles Obligatoires
- Français niveau A1 direct et vocabulaire professionnel de développeur.
- **Interdiction formelle de tout tableau Markdown** (`| ... |`) : utiliser exclusivement des listes à puces `- `.
- Liens relatifs exclusifs (`./`, `../`).
