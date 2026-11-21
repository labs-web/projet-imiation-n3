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

Chaque dossier de tutoriel contient :
- `[slug-tutoriel].md` : Document d'explication théorique ou compte-rendu des ateliers pratiques.
- `presentation-[slug-tutoriel].md` : Diaporama au format Marp Markdown pour la restitution orale (pour les formats `tuto-atelier`).
- `[slug-tutoriel].command.md` : Journal des commandes terminal exécutées (si manipulation CLI, hors git).
- Livrables pratiques spécifiques du tutoriel (ex : scripts, manifestes, code source).

*(Note : Aucun fichier `README.md` n'est créé dans les sous-dossiers de tutoriels unitaires pour éviter toute redondance avec `[slug-tutoriel].md`).*

---

## 3. Règles obligatoires
- Rédiger en français simple (niveau A1) avec le vocabulaire technique des développeurs.
- Interdiction formelle des tableaux Markdown (utiliser exclusivement des listes à puces `- `).
- Utiliser exclusivement des liens relatifs pour garantir la portabilité.
- Suivre le workflow normé documenté dans [Organisation des Livrables](../.agents/references/organisation-livrables.md).
- Maintenir l'arborescence miroir des versions dans `../.sync/`.

---

## 4. Domaines disponibles
- [scrum/](./scrum/) : Domaine Méthodes Agiles Scrum (`D.351.1-scrum`).
- [design/](./design/) : Domaine Conception & Design Thinking (`D.311.1-design`).
- [uml/](./uml/) : Domaine Modélisation UML & Conception Technique (`D.311.2-uml`).
- [architecture/](./architecture/) : Domaine Architecture logicielle modulaire (`D.312.1-architecture`).
- [laravel/](./laravel/) : Domaine Développement Backend Laravel 13 (`D.321.1-laravel`).
- [mobile/](./mobile/) : Domaine Client Mobile Android Natif Jetpack Compose (`D.323.1-mobile`).
- [devops/](./devops/) : Domaine Déploiement, DevOps & Packaging NativePHP (`D.341.1-devops`).
- [realisation-projet/](./realisation-projet/) : Domaine Réalisation et Conduite de Projet (`D.351.2-realisation-projet`).
