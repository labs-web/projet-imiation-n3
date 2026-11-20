# Règles de Gouvernance : Flux Générique et Flux de Sessions

Ce document définit les règles de collaboration et d'interface entre le skill de référence **`flux-travail`** et le skill pédagogique **`conception-session`**.

---

## 1. Séparation des Responsabilités (RACI)

- **Skill `flux-travail` (Gardien du Référentiel)** :
  - Propriétaire exclusif du flux universel d'ingénierie logicielle (`flux-travail/flux-travail-generique.md` - 25 étapes).
  - Responsable de la cohérence globale de l'espace `flux-travail/` et de ses guides méthodologiques (`flux-travail/docs/`).
  - Valide la conformité architecturale des sessions produites.
- **Skill `conception-session` (Ingénieur Pédagogique)** :
  - Concepteur opérationnel des flux de sessions (`flux-travail/sessions/flux-travail-s{N}.md`).
  - Découpe le projet d'imitation (*Blog des Lauréats*) en sprints de 80h.
  - Projette les intentions pédagogiques du concepteur sur les étapes du flux générique.

---

## 2. Règle d'Immuabilité du Référentiel Générique

- Le skill `conception-session` ne doit **jamais** modifier directement le fichier `flux-travail/flux-travail-generique.md`.
- Si la conception d'une session révèle le besoin d'une nouvelle étape générique ou d'une reformulation, la demande doit être transmise au skill `flux-travail`.
- Le flux générique reste le pivot immuable et stable pour toutes les sessions.

---

## 3. Typologie Obligatoire des Phases (`UA-Lab` vs `UA-Tâche`)

Chaque session de formation est obligatoirement découpée en phases typées :
- **Phase de type `UA-Lab`** :
  - S'applique dès qu'un domaine de compétence ou une notion technique nouvelle doit être assimilée.
  - Se compose obligatoirement de deux étapes consécutives :
    1. **Étape : Apprentissage** (notions théoriques et atelier guidé de référence).
    2. **Étape : Application sur le Blog** (mise en œuvre pratique immédiate dans le projet d'imitation *Blog des Lauréats*).
- **Phase de type `UA-Tâche`** :
  - S'applique lorsque la phase ne requiert aucun nouvel apport théorique (ex : rituels Scrum, gestion Git, préparation Discovery N+1, tests qualité DoD, revue, rétrospective).
  - Se compose **exclusivement d'étapes d'application opérationnelle**.

---

## 4. Règle de Précédence Temporelle de l'Apprentissage

- Chaque étape d'apprentissage (`UA-Lab`) doit impérativement précéder sa première utilisation en réalisation dans le sprint.
- Toutes les notions requises d'un même domaine pour la session sont consolidées dans l'étape d'apprentissage de cette phase UA-Lab.
- L'apprenant applique immédiatement sur le Blog ce qu'il vient d'assimiler dans l'atelier guidé.

---

## 5. Règle de Reprise Nominale Stricte

- Toute étape d'application dans une session doit porter l'intitulé exact de l'étape correspondante dans `flux-travail/flux-travail-generique.md`.
- Cette règle garantit la traçabilité complète entre le processus d'ingénierie universel et les activités de formation.

---

## 6. Cadre Tri-Projets et Évaluation

Chaque session structure la progression selon le cadre Tri-Projets :
- **Projet d'Imitation (*Blog des Lauréats*) :** Réalisé du Jour 1 au Jour 7 (conception, développement guidé et rituels).
- **Projet Technique (Portfolio personnel) :** Réalisé au Jour 8 en autonomie totale (codage pur sans conception, sanctionné par une épreuve de Live Coding de 40 minutes).
- **Projet Fil Rouge (Projet professionnel) :** Réalisé aux Jours 9 et 10 avec création de Skills agentiques réutilisables.

---

## 7. Formatage et Standards de Rédaction

- **Zéro tableau Markdown (`| ... |` formellement interdit) :** Utiliser exclusivement des listes à puces directes (`- `).
- **Zéro code numérique `UA.*` :** Utiliser des désignations descriptives claires (`UA-Lab : [Titre] (Domaine D.xxx.x)` ou `UA-Tâche : [Titre]`).
- **Un seul livrable principal unique par étape :** Identifié sous la mention `Sortie (1 seul livrable) : [chemin relatif]`.
- **Stack technique obligatoire :** Laravel 13, MySQL, Tailwind CSS avec Preline UI, Alpine.js, Antigravity Agent et GitHub Copilot.
