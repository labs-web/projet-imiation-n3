# Mission : Analyse des Remarques du Concepteur (`analyser-remarques.md`)

## 1. Objectif
Analyser les remarques, sélections de lignes et consignes méthodologiques fournies par le concepteur afin d'extraire les modifications précises à apporter sur le fichier cible et d'identifier l'ensemble des skills concernés.

---

## 2. Procédure d'Analyse

1. **Localiser le fichier et les lignes cibles :**
   - Identifier le fichier source visé (ex : `flux-travail/sessions/flux-travail-s0.md`).
   - Délimiter la plage de lignes sélectionnée par le concepteur (`L1-L238`).
   - Lire le contenu actuel de cette plage de lignes.

2. **Qualifier chaque remarque du concepteur :**
   - Décomposer le retour du concepteur en consignes unitaires.
   - Associer chaque consigne à une sous-section ou à un numéro de ligne précis.
   - Identifier la nature de la modification : ajout d'un prérequis, division d'une étape, renommage pour alignement générique, clarification d'une évaluation ou de la stack.

3. **Identifier les compétences et skills impactés :**
   - Si la remarque touche à la structure des sessions -> cibler `conception-session`.
   - Si la remarque touche aux 25 étapes universelles -> cibler `flux-travail`.
   - Si la remarque touche aux rôles Scrum ou prérequis de gouvernance -> cibler `domaine-scrum`.
   - Si la remarque touche à l'outillage ou aux règles IA -> cibler `domaine-ia`.
   - Si la remarque définit une nouvelle règle transverse -> cibler `.agents/rules/`.

4. **Transmettre les éléments qualifiés à la mission `generer-artefact-revision.md`.**
