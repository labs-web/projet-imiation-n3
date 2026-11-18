---
name: realisation-ua-lab
description: >-
  Réalise la partie théorique et la partie pratique d'un UA-Lab et dépose les livrables
  normalisés dans labs/[slug-domaine]/[slug-ua-lab]/ avec documentation et présentation Marp.
---

# Skill Réalisation : /realisation-ua-lab

## 1. Mission
Prendre en charge la réalisation complète d'un **UA-Lab** (bases théoriques et ateliers pratiques) à partir de sa fiche descriptive et produire tous les livrables normalisés dans le dépôt.

## 2. Déclenchement
- **Quand l'activer** :
  - Dès qu'un UA-Lab doit être réalisé pour satisfaire la *Base théorique et pratique* d'une étape de flux de travail.
  - Sur demande explicite avec l'URL ou le slug de l'UA-Lab (ex : `UA.351.11`).
- **Quand NE PAS l'activer** :
  - Pour une tâche de code propre à l'application du projet (utiliser les missions d'étapes).

## 3. Arborescence et livrables cibles
Tous les livrables sont déposés dans : `labs/[slug-domaine]/[slug-ua-lab]/`

Chaque UA-Lab produit obligatoirement 4 types de livrables :
- `README.md` : Fiche synthétique du lab (compétence, domaine, objectifs, index des livrables).
- `[slug-ua-lab].md` : Document d'explication complet combinant la théorie et les comptes-rendus pratiques.
- `presentation-[slug-ua-lab].md` : Diaporama au format Marp Markdown conçu via le skill `marp`.
- Livrables pratiques spécifiques : Fichiers produits lors des ateliers (charte, scripts, tests).

## 4. Procédure de réalisation pas-à-pas
- **Étape 1 : Cadrage** : Identifier le `[slug-domaine]`, le `[slug-ua-lab]`, la compétence et les tutoriels associés (théorique et pratique).
- **Étape 2 : Initialisation** : Créer le dossier cible et s'assurer que chaque niveau parent possède son `README.md`.
- **Étape 3 : Restitution théorique** : Rédiger la synthèse des concepts clés dans `[slug-ua-lab].md`.
- **Étape 4 : Génération Marp** : Créer la présentation `presentation-[slug-ua-lab].md` selon le skill `marp` avec la page de garde normalisée (Apprenant, Encadrant `ESSARRAJ Fouad`, Établissement `Solicode Tanger`).
- **Étape 5 : Réalisation pratique** : Exécuter les consignes des ateliers et produire les livrables d'application directe.
- **Étape 6 : Synthèse & Indexation** : Finaliser le fichier `README.md` local avec des liens relatifs vers chaque livrable.
- **Étape 7 : Contrôle qualité** : Vérifier l'absence totale de tableaux Markdown, la validité des liens relatifs et la clarté en français A1.
