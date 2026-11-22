# Mission : Couverture en Compétence d'une Étape de Sprint (`couvrir-etape-sprint.md`)

## 1. Contexte & Rôle
Cette mission intervient **au début de la réalisation d'une étape de sprint**, avant toute modification de code ou de livrable.
Elle garantit le respect de la règle d'ingénierie : **aucune étape de flux de travail n'est réalisée si sa mission et son skill associés n'existent pas au préalable**.

---

## 2. Règle de Granularité
- Une mission d'ingénierie peut être responsable d'**une seule étape** ou de **plusieurs étapes homogènes** du flux de travail (ex : une mission de cadrage couvrant la note de cadrage et la justification technique).
- Le regroupement est défini par `skills-planer` pour optimiser la cohérence et éviter l'émiettement.

---

## 3. Procédure Pas-à-Pas

1. **Audit Préalable de l'Étape à Réaliser :**
   - Identifier l'étape du flux de travail (`flux-travail/sessions/flux-travail-s{N}.md` ou `flux-travail-generique.md`).
   - Identifier le livrable attendu et la nature de l'activité (conception, cadrage, architecture, code Laravel, rituel).
   - Parcourir les skills existants (`.agents/skills/`) et leurs missions (`missions/`) pour vérifier si l'étape est déjà couverte.

2. **Arbitrage des 3 Options de Compétence :**
   Si l'étape n'est pas encore couverte ou si une adaptation est nécessaire, choisir l'option appropriée :
   - **Option A — Proposer un nouveau skill :**
     S'applique quand l'étape relève d'un domaine métier ou technique non représenté dans les skills existants (ex : `cadrage-produit`, `architecture-laravel`).
   - **Option B — Ajouter une mission dans un skill existant :**
     S'applique quand un skill pertinent existe déjà, mais nécessite une nouvelle mission pour prendre en charge cette étape (ou un groupe d'étapes liées).
   - **Option C — Proposer une reconception des skills :**
     S'applique quand l'architecture existante de compétences s'avère inadaptée, trop fragmentée ou redondante face au flux de travail.

3. **Émission de l'Artéfact Interactif de Proposition :**
   - Rédiger un artéfact interactif standardisé (`proposition-competence-[nom].md` avec `RequestFeedback: true`).
   - Présenter de manière claire :
     - L'étape du flux ciblée et son livrable.
     - L'option retenue (Nouveau skill / Ajout de mission / Reconception) avec justification.
     - La description du skill et de la (ou des) mission(s) associées, en précisant les étapes couvertes.
   - Attendre la validation explicite du concepteur (*Proceed*).

4. **Matérialisation et Déblocage de l'Exécution :**
   - Dès validation, exécuter `missions/creer-skill.md` pour initialiser le skill ou ajouter la mission dans le dossier correspondant.
   - Transmettre à `realisation-sprint` le feu vert pour exécuter l'étape avec son skill officiel.
