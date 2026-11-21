---
name: conception-ua-lab
description: >-
  Conçoit, découpe et séquence les Unités d'Apprentissage (UA-Lab) en tutoriels
  progressifs (tuto-labs, cas d'application épurés sans surcharge cognitive)
  à partir des intentions pédagogiques et des référentiels de compétences.
---

# Skill Conception UA-Lab : /conception-ua-lab

## 1. Mission
Concevoir l'ingénierie didactique d'une **Unité d'Apprentissage (UA-Lab)** en découpant le domaine en séquences progressives de tutoriels d'apprentissage (`tuto-lab`), en choisissant les cas d'application supports adaptés sans surcharge cognitive (ex : Todo List pour le Design Thinking), et en spécifiant les livrables attendus pour l'Agent Réalisation.

## 2. Déclenchement
- **Quand l'activer** :
  - Découpage didactique d'un domaine de compétence en plusieurs tutoriels unitaires progressifs (ex : Scrum en 5 labs, Design Thinking en 3 labs).
  - Choix et justification d'une application support épurée pour un atelier didactique.
  - Structuration de l'enchaînement logique d'une UA-Lab avant sa réalisation.
- **Quand NE PAS l'activer** :
  - Découpage et gouvernance de la session globale (`flux-travail-s{N}.md`) -> utiliser `conception-session`.
  - Rédaction effective et production des fiches de tutoriels et diaporamas Marp -> utiliser `realisation-ua-lab`.
  - Évolution des règles de compétences et méta-gouvernance -> utiliser `skills-dev`.

## 3. Structure canonique d'un Découpage d'UA-Lab
Pour chaque UA-Lab conçue, le skill définit :
- Les compétences et objectifs d'apprentissage visés (alignement sur le référentiel).
- L'enchaînement séquentiel des tutoriels d'apprentissage (`tuto-lab`) progressifs.
- Le choix motivé du support applicatif (justification pédagogique en cas d'application simplifiée).
- La liste des livrables requis par tutoriel (`[slug-tuto].md`, `presentation-[slug-tuto].md`, `[slug-tuto].command.md`).

## 4. Missions disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/decouper-ua-lab.md : Découpe une UA-Lab en tutoriels unitaires progressifs avec justification didactique des cas supports.
- missions/specifier-livrables-lab.md : Formalise le cahier des charges des livrables attendus pour l'agent de réalisation.
