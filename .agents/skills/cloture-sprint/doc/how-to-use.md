# Guide Opérationnel : Skill Clôture de Sprint (`/cloture-sprint`)

Ce guide formalise l'utilisation du skill **`cloture-sprint`** pour automatiser la conduite des cérémonies de fin de sprint et la production des documents officiels de suivi agile sous `sprints/` et `scrum/`.

---

## 1. Rôle du Skill
Le skill `cloture-sprint` intervient à la fin de chaque session/sprint pour assister l'équipe dans l'exécution ordonnée des 4 rituels de clôture :
1. **Sprint Review :** Validation interactive de l'incrément et audit des 7 critères de la Definition of Done.
2. **Sprint Retrospective :** Analyse réflexive, forces, freins et engagements d'amélioration continue.
3. **Backlog Refinement :** Clôture des User Stories terminées et réordonnancement du carnet de produit.
4. **Débriefing Individuel :** Auto-évaluation des compétences du sprint et débriefing du Live Coding.

---

## 2. Commandes d'Activation

- **/cloture-sprint review :**
  - Mission activée : `missions/sprint-review.md`
  - Livrable produit : `sprints/pv-review-[N].md`
- **/cloture-sprint retrospective :**
  - Mission activée : `missions/sprint-retrospective.md`
  - Livrable produit : `sprints/retrospective-[N].md`
- **/cloture-sprint refinement :**
  - Mission activée : `missions/backlog-refinement.md`
  - Livrable produit : `scrum/product-backlog.md`
- **/cloture-sprint debriefing :**
  - Mission activée : `missions/debriefing-session.md`
  - Livrable produit : `sprints/bilan-[N].md`

---

## 3. Prérequis d'Exécution
1. L'incrément logiciel du sprint doit être développé, testé en local et versionné sur la branche active (`sprintN`).
2. La feuille d'engagement du sprint est présente sous `sprints/sprint-[N].md`.
3. Le Product Backlog vivant est maintenu sous `scrum/product-backlog.md`.

---

## 4. Déroulement Pas-à-Pas
1. **Étape 1 — Revue :** Exécutez `/cloture-sprint review` avec l'incrément ouvert dans le navigateur. Vérifiez les 7 critères de la DoD et consignez le PV contradictoire.
2. **Étape 2 — Rétrospective :** Exécutez `/cloture-sprint retrospective` avec les membres de l'équipe pour identifier les réussites, freins et formaliser 2 actions d'amélioration.
3. **Étape 3 — Raffinement :** Exécutez `/cloture-sprint refinement` pour actualiser le carnet de produit dans `scrum/product-backlog.md` en préparation du sprint suivant.
4. **Étape 4 — Bilan individuel :** Exécutez `/cloture-sprint debriefing` pour consigner votre positionnement réflexif sur les compétences du cursus et débriefer le Live Coding (40 min).

---

## 5. Contrôle Qualité des Livrables
- Tous les documents générés sont rédigés en Markdown pur sans tableau Markdown.
- Les fichiers sont placés exclusivement sous les répertoires officiels `sprints/` et `scrum/`.
- Les noms de fichiers respectent la convention en minuscules avec le numéro du sprint (`pv-review-[N].md`, `retrospective-[N].md`).
