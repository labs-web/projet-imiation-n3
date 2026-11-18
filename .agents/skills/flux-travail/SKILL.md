---
name: flux-travail
description: >-
  Gère, insère et audite les étapes de réalisation dans flux-travail/flux-travail.md
  selon la structure normalisée à 4 sections. À utiliser pour faire évoluer le flux de travail.
---

# Skill Flux de Travail : /flux-travail

## 1. Mission
Piloter la structure, l'insertion et la mise à jour des étapes du projet dans `flux-travail/flux-travail.md` selon la démarche d'ingénierie logicielle (2TUP, Agile/Scrum).

## 2. Déclenchement
- **Quand l'activer** :
  - Ajout ou reformulation d'une étape de travail (depuis la description du concepteur ou les livrables produits).
  - Audit et restructuration globale de `flux-travail/flux-travail.md`.
- **Quand NE PAS l'activer** :
  - Exécution technique d'une tâche de code (utiliser le skill métier dédié).
  - Planification globale des sprints (utiliser `sprints/sprints.md`).

## 3. Structure normalisée d'une étape de flux
Chaque étape insérée doit obligatoirement respecter l'ordre des 4 sections :
- `## [N]. [Nom de l'étape]`
- `### Base théorique et pratique` (notions directes ou codes officiels `UA.*` fournis par le concepteur, aucun nom de lab inventé)
- `### Prérequis` (cadrage préalable, validation formateur ou livrables d'étapes antérieures)
- `### Travail à faire` (tâches opérationnelles ordonnées)
- `### Livrables` (dépôts, documentation, code, skills)

## 4. Procédure opératoire pas-à-pas
- **Étape 1 : Analyse de l'étape** : Extraire le numéro, l'intitulé, les prérequis réels, les tâches et les livrables attendus.
- **Étape 2 : Vérification anti-redondance** : S'assurer de l'absence de répétition entre *Base théorique et pratique* et *Prérequis*.
- **Étape 3 : Intégration dans le fichier** : Insérer l'étape dans la section de sprint correspondante dans `flux-travail/flux-travail.md`.
- **Étape 4 : Contrôle qualité** : Zéro tableau Markdown, liens relatifs purs, français A1.

## 5. Règles obligatoires
- Français A1 direct et vocabulaire professionnel de développeur.
- Aucun tableau Markdown (utiliser exclusivement des listes à puces `- `).
- Liens relatifs exclusifs (`./`, `../`).
