---
name: realisation-ua-lab
description: >-
  Réalise un UA-Lab en organisant ses livrables par sous-dossiers de tutoriels
  autonomes ([slug-tutoriel].md, presentation Marp) dans tutoriels/[domaine]/[ua]/.
---

# Skill Réalisation UA-Lab : /realisation-ua-lab

## 1. Mission
Prendre en charge la réalisation complète d'un **UA-Lab** en collaboration avec le skill de domaine correspondant (`domaine-[slug]`), et produire l'arborescence normalisée de livrables découpée par tutoriel.

## 2. Déclenchement
- **Quand l'activer** :
  - Réalisation d'une UA-Lab pour satisfaire la *Base théorique et pratique* d'une étape de flux de travail.
  - Demande explicite de réalisation d'un lab avec son URL ou son slug (ex : `UA.325.11`).
- **Quand NE PAS l'activer** :
  - Tâches applicatives du projet web Blog des lauréats (utiliser `gestion-depot` ou skills métier).
  - Évolution du référentiel méthodologique (utiliser `flux-travail`).

## 3. Structure modulaire obligatoire d'un UA-Lab
Tous les livrables sont déposés dans `tutoriels/[slug-domaine]/[slug-ua-lab]/` :
- **Fiche racine de l'UA-Lab (`README.md`)** : Cadrage pédagogique, objectifs, compétence et index des tutoriels.
- **Organisation en sous-dossiers de tutoriels (`[slug-tutoriel]/`)** :
  Chaque tutoriel possède son sous-dossier dédié contenant exclusivement :
  - `[slug-tutoriel].md` : Document technique complet (synthèse théorique ou compte-rendu d'atelier).
  - `presentation-[slug-tutoriel].md` : Diaporama au format Marp Markdown pour la soutenance orale.
  - Livrables pratiques éventuels (code, scripts, fichiers de configuration).
  *(Interdiction : Ne jamais créer de fichier `README.md` à l'intérieur des sous-dossiers de tutoriels).*

## 4. Procédure de réalisation pas-à-pas
- **Étape 1 : Cadrage avec le skill de domaine** : Consulter `domaine-[slug]` pour identifier la compétence, les étapes d'apprentissage et les notions de base.
- **Étape 2 : Initialisation de l'arborescence** : Créer le dossier racine de l'UA-Lab avec son `README.md` d'indexation.
- **Étape 3 : Production par sous-dossier de tutoriel** :
  - Créer le dossier du tutoriel `[slug-tutoriel]/`.
  - Rédiger la fiche de contenu `[slug-tutoriel].md` (zéro tableau, liens relatifs, français A1).
  - Concevoir le diaporama Marp `presentation-[slug-tutoriel].md` avec page de garde Solicode (Encadrant ESSARRAJ Fouad).
  - Ne pas créer de fichier `README.md` dans ce sous-dossier.
- **Étape 4 : Indexation parent** : Mettre à jour le fichier `README.md` à la racine de l'UA-Lab avec les liens relatifs vers chaque livrable de tutoriel.
- **Étape 5 : Contrôle qualité** : Vérifier l'absence totale de tableaux Markdown, la validité des liens relatifs, et laisser les fichiers prêts pour commit par le concepteur.
