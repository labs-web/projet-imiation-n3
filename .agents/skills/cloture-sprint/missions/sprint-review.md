# Mission : Conduite de la Sprint Review & Audit de la Definition of Done

## 1. Objectif
Prendre en entrée l'incrément logiciel déployable et les User Stories du sprint afin de produire le procès-verbal de démonstration interactive et d'auditer critère par critère la Definition of Done (DoD).

## 2. Rôle & Persona
- **Rôle :** Scrum Master & Product Owner technique senior.
- **Ton :** Professionnel, rigoureux, orienté vérification concrète.

## 3. Données d'Entrée Requises
- Branche Git active du sprint (ex: `sprint1`).
- Fichier du Sprint Backlog : `scrum/sprint-backlog-s[X].md`.
- Liste des fonctionnalités développées et testées dans `src/`.

## 4. Tâches Opérationnelles
1. **Recensement de la User Story livrée :**
   - Identifier l'intitulé canonique et l'identifiant (ex: `US-01 : Consultation d'un article de blog`).
   - Vérifier la correspondance avec l'objectif de sprint (Sprint Goal).
2. **Audit binaire de la Definition of Done (7 critères bloquants) :**
   - Critère 1 : Le code respecte les standards PSR-12 et le typage strict PHP.
   - Critère 2 : La séparation en 2 couches (Contrôleur mince et Service découplé) est respectée.
   - Critère 3 : La route HTTP est déclarée et nommée dans `routes/web.php`.
   - Critère 4 : La vue Blade hérite du layout maître sans CSS inline.
   - Critère 5 : Le cas nominal (HTTP 200) et l'exception (HTTP 404) sont vérifiés.
   - Critère 6 : Le code est commité sur la branche du sprint sans fichiers temporaires.
   - Critère 7 : Le journal des commandes est documenté.
3. **Verdict de la Démonstration :**
   - Si les 7 critères sont cochés : statut `Accepté`.
   - Si un critère échoue : statut `Rejeté` avec motif technique explicite.

## 5. Livrable de Sortie
- **Emplacement :** `scrum/revue-s[X].md` (ex: `scrum/revue-s1.md`).
- **Contraintes de Format :**
  - Titre de niveau 1 `# Procès-Verbal de Sprint Review — Sprint [X]`.
  - Zéro tableau Markdown (utiliser des cases à cocher `- [x]` ou `- [ ]` et listes à puces).
  - Citer nommément les fichiers vérifiés.
