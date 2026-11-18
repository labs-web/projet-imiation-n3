# Guide Opérationnel : Skill Clôture de Sprint (`/cloture-sprint`)

Ce guide formalise l'utilisation du skill **`cloture-sprint`** pour automatiser la conduite des cérémonies de fin de sprint et la production des documents officiels de suivi agile sous `scrum/` et `issues/`.

---

## 1. Rôle du Skill
Le skill `cloture-sprint` intervient à la fin de chaque session/sprint pour assister l'équipe dans l'exécution ordonnée des 4 rituels de clôture :
1. **Sprint Review :** Validation interactive de l'incrément et audit binaire de la Definition of Done.
2. **Sprint Retrospective :** Analyse réflexive, forces, freins et détection de dettes méthodologiques.
3. **Backlog Refinement :** Archivage des issues complétées et préparation du sprint suivant.
4. **Débriefing Individuel :** Auto-évaluation des 5 compétences du sprint et débriefing du Live Coding.

---

## 2. Commandes d'Activation

| Commande | Mission Activée | Livrable Produit |
| :--- | :--- | :--- |
| `/cloture-sprint review` | `missions/sprint-review.md` | `scrum/revue-s[X].md` |
| `/cloture-sprint retrospective` | `missions/sprint-retrospective.md` | `scrum/retrospective-s[X].md` |
| `/cloture-sprint refinement` | `missions/backlog-refinement.md` | `issues/issues-closes.md` & `scrum/product-backlog.md` |
| `/cloture-sprint debriefing` | `missions/debriefing-session.md` | `scrum/bilan-s[X].md` |

---

## 3. Prérequis d'Exécution
1. L'incrément logiciel du sprint doit être développé, testé en local et versionné sur la branche active (`sprintX`).
2. Les tâches du sprint sont répertoriées dans `issues/issues-open.md`.
3. Le Sprint Backlog du sprint est présent sous `scrum/sprint-backlog-s[X].md`.

---

## 4. Déroulement Pas-à-Pas
1. **Étape 1 — Revue :** Exécutez `/cloture-sprint review` avec l'incrément ouvert dans le navigateur. Vérifiez les 7 critères de la DoD.
2. **Étape 2 — Rétrospective :** Exécutez `/cloture-sprint retrospective` avec les membres de l'équipe pour identifier les forces, freins et acter le constat de dette d'empathie utilisateur.
3. **Étape 3 — Raffinement :** Exécutez `/cloture-sprint refinement` pour transférer la User Story dans `issues/issues-closes.md` et réordonner le backlog pour le sprint suivant.
4. **Étape 4 — Bilan individuel :** Exécutez `/cloture-sprint debriefing` pour consigner votre positionnement réflexif sur les 5 compétences du cursus et débriefer le Live Coding (40 min).

---

## 5. Contrôle Qualité des Livrables
- Tous les documents générés sont rédigés en Markdown pur sans tableau Markdown.
- Les fichiers sont placés exclusivement sous les répertoires `scrum/` et `issues/`.
- Les noms de fichiers respectent la convention en minuscules avec le numéro du sprint (`revue-s1.md`, `retrospective-s1.md`, `bilan-s1.md`).
