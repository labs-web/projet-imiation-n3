# Dossier du Flux de Travail (`flux-travail/`)

Ce dossier est le centre névralgique de gouvernance méthodologique du projet. Il structure et documente la démarche de réalisation du logiciel et la progression pédagogique par session.

---

## 1. Organisation du Dossier

Le dossier sépare rigoureusement la dimension d'ingénierie logicielle universelle et la dimension didactique de formation par session :

- **[flux-travail.md](./flux-travail.md)** : Hub d'accueil et d'orientation présentant l'articulation des référentiels.
- **[flux-travail-generique.md](./flux-travail-generique.md)** : Référentiel universel d'ingénierie logicielle en 25 étapes (Sprint 0 Cadrage & Socle, Cycle Dual-Track Sprint $N$ avec pistes Discovery et Delivery, et Clôture/Déploiement final). Valable pour tout projet de développement web basé sur Laravel 13, MySQL, Tailwind CSS avec Preline UI, Alpine.js et Git.
- **[sessions/](./sessions/)** : Répertoire contenant les flux de travail opérationnels pour chaque session de formation N3 (de S0 à S8). Chaque session alterne directement les UA-labs d'apprentissage avec les étapes de réalisation concrètes :
  - `sessions/README.md` : Index complet des 9 sessions avec leurs objectifs d'apprentissage et la table de correspondance avec les 25 étapes du flux générique.
  - `sessions/flux-travail-s0.md` : Fiche détaillée du Sprint 0 (19 étapes chronologiques intercalées).
  - `sessions/flux-travail-s1.md` : Fiche détaillée du Sprint 1 (13 étapes chronologiques intercalées et Live Coding 40 min).
- **[docs/](./docs/)** : Répertoire contenant les 5 guides méthodologiques thématiques de référence :
  - `01-referentiel-methodes.md` : Les 4 méthodes (DT, GP, Dev OO, Scrum) et la définition formelle du User Flow.
  - `02-cycle-dual-track.md` : Guide opérationnel du cycle Dual-Track Agile (Discovery & Delivery).
  - `03-sprint-0-cadrage.md` : Guide pratique pour mener le Sprint 0 (cadrage, UI Kit, maquettes et socle).
  - `04-norme-etapes-pedagogiques.md` : Spécification de l'intercalage pédagogique synchrone des UA-labs.
  - `05-outillage-agent-ia.md` : Guide d'accompagnement par l'Agent IA à chaque étape du flux.

---

## 2. Règles de Contribution

- **Zéro tableau Markdown** : L'utilisation de tableaux Markdown (`| ... |`) est formellement interdite. Utiliser exclusivement des listes à puces directes (`- `).
- **Liens relatifs exclusifs** : Tous les liens doivent être relatifs (`./`, `../`) pour garantir la portabilité sur GitHub.
- **Niveau de français A1** : Phrases courtes, actives et directes (Sujet + Verbe + Complément) avec le vocabulaire technique des développeurs.
