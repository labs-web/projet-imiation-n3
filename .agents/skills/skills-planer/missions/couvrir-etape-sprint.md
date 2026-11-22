# Mission : Couverture en Compétence d'une Étape de Sprint (`couvrir-etape-sprint.md`)

## 1. Contexte & Rôle
Cette mission intervient **au début de la réalisation d'une étape de sprint**, avant toute modification de code ou de livrable.
Elle garantit deux impératifs méthodologiques fondamentaux :
1. **Aucune étape de flux de travail n'est réalisée sans compétence dédiée préalable** (skill et mission existants).
2. **Critique systématique du plan préliminaire :** Même si `docs/plan-preliminaire-skills.md` existe, l'agent ne l'applique jamais aveuglément ; il critique ce qui était prévu et propose une solution supérieure, plus fine et mieux ajustée à la réalité du sprint.

---

## 2. Règle de Granularité
- Une mission d'ingénierie peut être responsable d'**une seule étape** ou de **plusieurs étapes homogènes** du flux de travail (ex : une mission de cadrage couvrant la note de cadrage et la justification technique).
- Le regroupement est défini par `skills-planer` pour optimiser la cohésion métier et éviter la dispersion.

---

## 3. Procédure Pas-à-Pas

1. **Audit Préalable de l'Étape à Réaliser :**
   - Identifier l'étape du flux de travail (`flux-travail/sessions/flux-travail-s{N}.md` ou `flux-travail-generique.md`).
   - Identifier le livrable attendu et la nature de l'activité (conception, cadrage, architecture, code Laravel, rituel).
   - Vérifier si un skill et une mission existants couvrent déjà cette étape.

2. **Critique Systématique du Plan Préliminaire (`docs/plan-preliminaire-skills.md`) :**
   - Si `docs/plan-preliminaire-skills.md` existe, examiner ce qui y avait été initialement prévu pour cette étape.
   - Identifier les limites, approximations théoriques ou rigidités du plan initial au regard du travail concret demandé par le concepteur.
   - Formuler explicitement les arguments montrant pourquoi la nouvelle proposition surpasse le plan préliminaire (meilleure cohésion, moins de dépendances, livrables plus nets, responsabilités clarifiées).

3. **Arbitrage des 3 Options d'Évolution :**
   Concevoir l'organisation optimale en choisissant l'option idoine :
   - **Option A — Proposer un nouveau skill :**
     Quand l'étape relève d'un domaine métier ou technique non outillé (ex : `cadrage-produit`, `architecture-laravel`).
   - **Option B — Ajouter une mission dans un skill existant :**
     Quand un skill pertinent existe déjà et qu'il est plus cohérent d'y agréger la mission (une mission pouvant couvrir plusieurs étapes).
   - **Option C — Proposer une reconception des skills :**
     Quand l'architecture existante de compétences s'avère morcelée ou redondante face aux exigences de l'étape.

4. **Émission de l'Artéfact Interactif de Proposition :**
   - Rédiger un artéfact interactif standardisé (`proposition-competence-[nom].md` avec `RequestFeedback: true`).
   - Présenter obligatoirement :
     - L'étape du flux ciblée et son livrable unique attendu.
     - **La section critique du plan préliminaire** : limites de la prévision initiale et gains de la solution proposée.
     - L'option retenue (Nouveau skill / Ajout de mission / Reconception) avec justification détaillée.
     - La description du skill et de ses missions, avec les étapes couvertes.
   - Attendre la validation formelle du concepteur (*Proceed*).

5. **Matérialisation et Déblocage de l'Exécution :**
   - Dès validation, exécuter `missions/creer-skill.md` pour matérialiser le skill ou ajouter la mission.
   - Donner le feu vert à `realisation-sprint` pour exécuter l'étape avec son skill officiel.
