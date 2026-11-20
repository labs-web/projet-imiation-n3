# Règles de Gouvernance : Flux Générique et Flux de Sessions

Ce document définit les règles de collaboration et d'interface entre le skill de référence **`flux-travail`** et le skill pédagogique **`conception-session`**.

---

## 1. Séparation des Responsabilités (RACI)

- **Skill `flux-travail` (Gardien du Référentiel)** :
  - Propriétaire exclusif du flux universel d'ingénierie logicielle (`flux-travail/flux-travail-generique.md`).
  - Responsable de la cohérence globale de l'espace `flux-travail/` et de ses guides méthodologiques (`flux-travail/docs/`).
  - Valide la conformité architecturale des sessions produites.
- **Skill `conception-session` (Ingénieur Pédagogique)** :
  - Concepteur opérationnel des flux de sessions (`flux-travail/sessions/flux-travail-s{N}.md`).
  - Découpe le projet d'imitation (*Blog des Lauréats*) en sessions opérationnelles.
  - Projette les intentions pédagogiques du concepteur sur les étapes du flux générique.

---

## 2. Règle d'Immuabilité du Référentiel Générique

- Le skill `conception-session` ne doit **jamais** modifier directement le fichier `flux-travail/flux-travail-generique.md`.
- Si la conception d'une session révèle le besoin d'une nouvelle étape générique ou d'une reformulation, la demande doit être transmise au skill `flux-travail`.
- Le flux générique reste le pivot immuable et stable pour toutes les sessions.

---

## 3. Typologie des Phases et Règle des 3 UA-Tâches Maximum

Chaque session de formation est découpée en phases typées :
- **Phase de type `UA-Lab`** :
  - S'applique dès qu'un domaine de compétence ou une notion technique nouvelle doit être assimilée.
  - Se compose de :
    1. **Étape : Tutoriel-lab : [Intitulé]** : Apprentissage théorique et atelier guidé. Produit **obligatoirement 2 livrables** :
       - Un guide explicatif détaillé au format Markdown (`guide-[nom].md`).
       - Un support de présentation de diapositives au format Marp Markdown (`presentation-[nom].md`).
    2. **Étape : Tutoriel-application : [Intitulé]** : Application directe et immédiate sur le Blog des Lauréats. Une étape d'application n'appartient à un UA-Lab que si elle découle directement de l'atelier du lab.
- **Phase de type `UA-Tâche` (3 blocs au maximum par session)** :
  - S'applique lorsque les activités ne requièrent aucun apport théorique synchrone.
  - Afin d'éviter la dispersion et de respecter l'ordre naturel du flux générique, les UA-Tâches sont groupées en **3 blocs au maximum** :
    1. **UA-Tâche Début :** Lancement, cadrage initial et préparation de l'environnement (Git, README).
    2. **UA-Tâche Milieu :** Activités transverses de modélisation ou de préparation Discovery non issues d'un lab synchrone.
    3. **UA-Tâche Fin :** Clôture de session, Qualité DoD, Sprint Review et Sprint Retrospective.

---

## 4. Titres Épurés et Référence Générique dans le Corps

- **Titres épurés :** Le titre d'une étape (`### Étape X : [Titre]`) ne doit **jamais** afficher la mention générique (ex: `(Étape Générique N)` proscrit dans les en-têtes).
- **Traçabilité en description :** La correspondance avec le flux générique est obligatoirement explicitée au début du corps de l'étape : `- Correspondance flux générique : Étape Générique N ([Nom exact générique])`.

---

## 5. Règle de Précédence Temporelle de l'Apprentissage

- Chaque étape d'apprentissage (`UA-Lab`) doit impérativement précéder sa première utilisation en réalisation dans le sprint.
- Toutes les notions requises d'un même domaine pour la session sont consolidées dans l'étape d'apprentissage de cette phase UA-Lab.
- L'apprenant applique immédiatement sur le Blog ce qu'il vient d'assimiler dans l'atelier guidé.

---

## 6. Cadre Tri-Projets et Durées Indicatives

Chaque session structure la progression selon le cadre Tri-Projets :
- **Projet d'Imitation (*Blog des Lauréats*) :** Réalisation pas-à-pas en classe active (conception, développement guidé et rituels). Le projet d'imitation est exclusivement le Blog (la TodoList ne servant que d'exemple didactique en tutoriel).
- **Projet Technique (Portfolio personnel) :** Réalisé en fin d'itération en autonomie totale (codage technique pur sans conception lors des sprints de delivery).
- **Projet Fil Rouge (Projet professionnel) :** Réalisé en clôture d'itération avec création de Skills agentiques réutilisables dans `.agent/skills/`.
- **Durées indicatives :** Les mentions de 80 heures et 10 jours sont fournies à titre indicatif pour les formateurs et le concepteur ; l'agent IA ne doit pas les contraindre de manière rigide.

---

## 7. Formatage et Standards de Rédaction

- **Zéro tableau Markdown (`| ... |` formellement interdit) :** Utiliser exclusivement des listes à puces directes (`- `).
- **Zéro code numérique `UA.*` :** Utiliser des désignations descriptives claires (`UA-Lab : [Titre] (Domaine D.xxx.x)` ou `UA-Tâche : [Titre]`).
- **Stack technique obligatoire :** Laravel 13, MySQL, Tailwind CSS avec Preline UI, Alpine.js, Antigravity Agent et GitHub Copilot.
