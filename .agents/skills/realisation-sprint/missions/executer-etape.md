# Mission : Exécution Pas-à-Pas d'une Étape de Jalon (`executer-etape.md`)

## 1. Contexte & Rôle
Après validation du plan de jalon par le concepteur, cette mission pilote la réalisation unitaire de chaque étape du jalon selon un protocole strict et ordonné en 4 temps.

---

## 2. Protocole Obligatoire en 4 Temps par Étape

Pour chaque étape du flux de travail à réaliser :

1. **Temps 1 — Convocation Obligatoire de `skills-planer` :**
   - Identifier l'étape du flux de travail et le livrable attendu.
   - Convoquer immédiatement le skill `skills-planer` (mission `couvrir-etape-sprint.md`).
   - `skills-planer` critique le plan préliminaire (`docs/plan-preliminaire-skills.md`) et conçoit la compétence requise (nouveau skill, mission dans un skill existant, ou reconception).

2. **Temps 2 — Création Physique Immédiate de la Compétence :**
   - `skills-planer` matérialise physiquement l'arborescence et les fichiers (`SKILL.md` $\le 75$ lignes et missions associées).

3. **Temps 3 — Soumission de la Compétence à Validation du Concepteur :**
   - Émettre un artéfact interactif standardisé (`validation-skill-[nom].md` avec `RequestFeedback: true`).
   - Présenter au concepteur : la compétence créée, ses fichiers, sa justification, et la critique du plan préliminaire.
   - Suspendre toute modification en attente du clic sur *Proceed* par le concepteur.

4. **Temps 4 — Réalisation Concrète de l'Étape :**
   - Dès la compétence validée, mobiliser le skill créé pour exécuter l'étape d'ingénierie.
   - Produire le livrable unique au format exigé (Laravel 13, MySQL, Tailwind/Preline, A1/A2, zéro tableau, liens relatifs).
   - Mettre à jour le suivi d'avancement du sprint (`sprints/sprint-[N].md`).
   - Passer à l'étape suivante du jalon en répétant le protocole, ou clore le jalon via `missions/valider-jalon.md`.
