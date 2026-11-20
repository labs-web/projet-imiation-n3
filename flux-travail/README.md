# Dossier du Flux de Travail (`flux-travail/`)

Ce dossier est le centre névralgique de gouvernance méthodologique du projet. Il structure et documente la démarche de réalisation du logiciel et la progression pédagogique.

---

## 1. Organisation du Dossier

Le dossier sépare rigoureusement la dimension d'ingénierie logicielle et la dimension didactique de formation :

- **[flux-travail.md](./flux-travail.md)** : Hub d'accueil et d'orientation présentant l'articulation des deux flux.
- **[flux-travail-generique.md](./flux-travail-generique.md)** : Référentiel universel d'ingénierie logicielle en 16 étapes (Sprint 0, Cycle Dual-Track Sprint $N$ avec pistes Discovery et Delivery, et Clôture/Déploiement final). Valable pour tout projet de développement web basé sur Laravel 12, Alpine.js et Tailwind CSS.
- **[flux-travail-pedagogique.md](./flux-travail-pedagogique.md)** : Guide d'apprentissage pour les sessions de formation Solicode Niveau 3. Il découpe la session de formation selon le format standard à 4 sections (*Base théorique/UAs*, *Prérequis*, *Travail à faire*, *Livrables*) en référençant le flux générique sans le dupliquer.
- **[docs/](./docs/)** : Répertoire contenant les 5 guides méthodologiques thématiques de référence :
  - `01-referentiel-methodes.md` : Les 4 méthodes (DT, GP, Dev OO, Scrum) et la définition formelle du User Flow.
  - `02-cycle-dual-track.md` : Guide opérationnel du cycle Dual-Track Agile (Discovery & Delivery).
  - `03-sprint-0-cadrage.md` : Guide pratique pour mener le Sprint 0 (cadrage, UI Kit, maquettes et socle).
  - `04-norme-etapes-pedagogiques.md` : Spécification du format standardisé à 4 sections des étapes didactiques.
  - `05-outillage-agent-ia.md` : Guide d'accompagnement par l'Agent IA à chaque étape du flux.

---

## 2. Règles de Contribution

- **Zéro tableau Markdown** : L'utilisation de tableaux Markdown (`| ... |`) est formellement interdite. Utiliser exclusivement des listes à puces directes (`- `).
- **Liens relatifs exclusifs** : Tous les liens doivent être relatifs (`./`, `../`) pour garantir la portabilité sur GitHub.
- **Niveau de français A1** : Phrases courtes, actives et directes (Sujet + Verbe + Complément) avec le vocabulaire technique des développeurs.
