# Norme des Étapes et Livrables Pédagogiques (Format Standard à 4 Sections)

Ce document définit la structure normalisée obligatoire pour toute étape intégrée dans le flux de travail pédagogique des sessions de formation.

---

## 1. Principes Didactiques Fondamentaux

Le flux pédagogique adapte le flux d'ingénierie logicielle pour encadrer la progression d'un apprenant :

- **Approche par compétences** : Chaque étape est rattachée à une ou plusieurs Unités d'Apprentissage certifiantes (`UA.*`).
- **Principe de Pareto 20/80** : La théorie se limite aux 20% de concepts indispensables. Les 80% restants sont acquis par la recherche active et la pratique sur le projet d'imitation.
- **Élimination des cours redondants** : Ne jamais réenseigner des notions déjà validées aux niveaux antérieurs (ex: bases de Git, HTML basique, manipulation de terminal).

---

## 2. Structure Normalisée à 4 Sections

Toute étape pédagogique doit obligatoirement respecter l'ordre et le contenu des 4 sections suivantes :

```markdown
## [Numéro]. [Titre explicite de l'étape]

### Base théorique et pratique
- Codes et intitulés des Unités d'Apprentissage officielles (ex: UA.325.11, UA.351.11).
- Liens relatifs vers les fiches tutoriels de référence dans `tutoriels/` ou `_tutos/`.

### Prérequis
- Validation préalable par le formateur référent.
- Compétences acquises ou livrables issus des étapes précédentes indispensables pour démarrer.

### Travail à faire
- Liste ordonnée des tâches pratiques à réaliser par l'apprenant.
- Formulation des actions précises à accomplir avec ou sans l'assistance de l'Agent IA.

### Livrables
- Liste exhaustive des fichiers physiques produits (fiches de synthèse, présentations Marp, code source, tests).
- Enregistrement des versions dans `.sync/.../version.yml`.
```

---

## 3. Typologie des Unités d'Apprentissage (UA)

Le flux distingue deux catégories d'activités pédagogiques :

- **UA-Lab (Atelier guidé avec assimilation conceptuelle)** :
  - Concerne les nouvelles notions techniques ou architecturales (ex: Architecture 2 couches, Prompt Engineering RIO, Laravel 12).
  - Comporte une synthèse personnelle théorique (20/80) et un atelier pratique guidé.
  - Livrable obligatoire : Fiche technique `.md`, diaporama Marp `.md` et code source.
- **UA-Tâche (Action opérationnelle pure)** :
  - Concerne les rituels de gestion et les actions outillées sans cours théorique lourd (ex: Cadrage Scrum, Sprint Planning, Daily Scrum, Sprint Review, Rétrospective).
  - 100% orienté sur l'action immédiate.
  - Livrable : Fiche de compte-rendu, journal de commandes ou fichier de gestion d'issues.

---

## 4. Règles de Qualité des Livrables

- **Zéro tableau Markdown** : Utiliser exclusivement des listes à puces directes (`- `).
- **Liens relatifs portables** : Ne jamais employer de chemins absolus (`C:\...`, `D:\...`).
- **Français niveau A1** : Rédiger des phrases courtes, directes et claires (Sujet + Verbe + Complément).
- **Diaporamas Marp** : Format Marp Markdown strict avec page de garde Solicode normalisée (Nom apprenant, formateur ESSARRAJ Fouad, domaine et compétence).
