# Dossier des Tutoriels (`tutoriels/`)

Ce dossier regroupe tous les tutoriels d'apprentissage réalisés pour acquérir les bases théoriques et pratiques nécessaires au projet.

---

## 1. Organisation du dossier

Les tutoriels sont organisés par domaine de formation puis par unité d'apprentissage :
- `tutoriels/[slug-domaine]/` : Regroupe les tutoriels rattachés à un même domaine de compétence.
- `tutoriels/[slug-domaine]/[slug-ua]/` : Regroupe les tutoriels rattachés à une même unité d'apprentissage.
- `tutoriels/[slug-domaine]/[slug-ua]/[slug-tutoriel]/` : Dossier spécifique d'un tutoriel contenant ses livrables complets.

---

## 2. Structure type d'un tutoriel

Chaque dossier de tutoriel contient obligatoirement :
- `README.md` : Fiche synthétique du tutoriel (contexte, compétence visée, objectifs pédagogiques, index des livrables).
- `[slug-tutoriel].md` : Document d'explication théorique et compte-rendu des ateliers pratiques.
- `presentation-[slug-tutoriel].md` : Diaporama au format Marp Markdown pour la restitution orale.
- Livrables pratiques spécifiques du tutoriel (ex : scripts, maquettes, code source).

---

## 3. Règles obligatoires
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- Interdiction formelle des tableaux Markdown (utiliser exclusivement des listes à puces `- `).
- Utiliser exclusivement des liens relatifs pour garantir la portabilité.
