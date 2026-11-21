# Mission : Spécifier les Livrables d'un UA-Lab

## 1. Contexte & Objectif
Cette mission produit le cahier des charges des livrables attendus pour chaque tutoriel d'une UA-Lab à destination de l'agent `realisation-ua-lab`.

## 2. Spécification Normative
Pour chaque tutoriel de l'UA-Lab, spécifier :
- L'arborescence cible : `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/`.
- La fiche technique : `[slug-tuto].md` (notions théoriques consolidées, démarche, exercices).
- Le diaporama Marp : `presentation-[slug-tuto].md` avec page de garde normalisée EFP.
- Le journal CLI : `[slug-tuto].command.md` si des commandes terminal sont requises.
- Le statut de versioning initial pour `.sync/tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/version.yml`.
