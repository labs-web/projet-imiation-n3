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
Tous les livrables sont déposés dans `tutoriels/[slug-domaine]/[slug-ua-lab]/[slug-tutoriel]/` :
- **Règle Unique du fichier `README.md`** : Le fichier `README.md` est requis **exclusivement à la racine du dossier `tutoriels/`** (`tutoriels/README.md`) pour en présenter la structure globale.
- **Interdiction absolue** de créer des fichiers `README.md` intermédiaires dans les sous-dossiers de domaines (`[slug-domaine]/`), d'UA-Labs (`[slug-ua-lab]/`) ou de tutoriels (`[slug-tutoriel]/`).
- **Organisation en sous-dossiers de tutoriels (`[slug-tutoriel]/`)** :
  Chaque tutoriel possède son sous-dossier dédié contenant exclusivement :
  - `[slug-tutoriel].md` : Document technique complet portant directement le nom du slug (synthèse théorique ou compte-rendu d'atelier).
  - `presentation-[slug-tutoriel].md` : Diaporama au format Marp Markdown pour la soutenance orale.
  - `[slug-tutoriel].command.md` : Journal des commandes terminal exécutées (obligatoire pour tuto-lab, tuto-notion, tuto-code s'il y a des commandes ; formellement exclu pour tuto-tache).
  - Livrables pratiques éventuels (code, scripts, fichiers de configuration).

## 4. Procédure de réalisation pas-à-pas
- **Étape 1 : Cadrage avec le skill de domaine** : Consulter `domaine-[slug]` et `.agents/references/gestion-livrables.md` pour identifier la compétence, les étapes d'apprentissage, l'emplacement et les notions de base.
- **Étape 2 : Initialisation de l'arborescence** : Créer l'arborescence `tutoriels/[slug-domaine]/[slug-ua-lab]/[slug-tutoriel]/` sans aucun fichier `README.md` intermédiaire.
- **Étape 3 : Production par sous-dossier de tutoriel** :
  - Créer le dossier du tutoriel `[slug-tutoriel]/`.
  - Rédiger la fiche de contenu `[slug-tutoriel].md` (zéro tableau, liens relatifs, français A1).
  - Concevoir le diaporama Marp `presentation-[slug-tutoriel].md` avec page de garde Solicode (Encadrant ESSARRAJ Fouad).
  - Rédiger le journal de commandes CLI `[slug-tutoriel].command.md` si des commandes sont exécutées (sans commandes git).
  - Déclarer la traçabilité de version dans `.sync/tutoriels/[slug-domaine]/[slug-ua-lab]/[slug-tutoriel]/version.yml`.
  - Ne créer aucun fichier `README.md` dans ce sous-dossier ou ses parents.
- **Étape 4 : Indexation centrale** : Référencer le tutoriel dans le fichier d'accueil unique `tutoriels/README.md` avec ses liens relatifs.
- **Étape 5 : Contrôle qualité** : Vérifier l'absence totale de tableaux Markdown, l'absence de `README.md` parasites, la validité des liens relatifs, et laisser les fichiers prêts pour commit par le concepteur.
