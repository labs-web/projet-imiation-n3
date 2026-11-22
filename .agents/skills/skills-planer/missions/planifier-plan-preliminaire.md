# Mission : Planification Préliminaire Globale des Compétences (`planifier-plan-preliminaire.md`)

## 1. Contexte & Rôle
Cette mission analyse le [flux-travail-generique.md](../../../flux-travail/flux-travail-generique.md) (les 25 étapes universelles d'ingénierie logicielle) pour concevoir un **plan préliminaire d'architecture des compétences**.
Ce plan ne crée pas les skills immédiatement : il sert de boussole et de guide méthodologique pour la planification progressive lors des sprints.

---

## 2. Emplacement du Livrable Validé
- **Règle absolue :** Le document de référence validé est déposé dans l'espace documentaire du projet :
  - Chemin : `docs/plan-preliminaire-skills.md`.
  - Il ne doit **jamais** être stocké dans le dossier `.agents/skills/skills-planer/`.

---

## 3. Procédure Pas-à-Pas

1. **Analyse du Flux Générique (25 étapes) :**
   - Parcourir les 3 macro-phases : Sprint 0 (Cadrage, Design Macro), Cycle Itératif Dual-Track (Sprint N), et Phase Finale (Livraison & Clôture).
   - Identifier pour chaque étape : les compétences requises, les activités d'ingénierie et le livrable unique attendu.

2. **Regroupement de Niveau 1 (Missions dans des Skills Métiers) :**
   - Regrouper les étapes en compétences thématiques cohérentes :
     - Cadrage & Gestion de Projet (Étapes 1, 3, 4).
     - Infrastructure & Configuration Git (Étape 2).
     - Design Thinking & UI Kit (Étapes 5, 6, 8, 9, 19).
     - Product Backlog & Rituels Scrum (Étapes 7, 15, 18, 20).
     - Architecture & Développement Backend Laravel (Étapes 12, 13, 14, 17).
     - Qualité, Tests & DoD (Étape 21).
     - Clôture de Sprint & Rétrospective (Étapes 10, 11, 22, 23).
     - Recette, Déploiement & Bilan Projet (Étapes 24, 25).

3. **Génération de l'Artéfact Interactif de Proposition :**
   - Générer un artéfact interactif standardisé (`plan-preliminaire-skills.md` avec `RequestFeedback: true`).
   - Présenter la matrice de couverture des 25 étapes et le rôle attendu de chaque compétence.
   - Demander la validation formelle du concepteur via le bouton *Proceed*.

4. **Consignation Documentaire :**
   - Dès validation par le concepteur, copier/enregistrer le document sous `docs/plan-preliminaire-skills.md`.
