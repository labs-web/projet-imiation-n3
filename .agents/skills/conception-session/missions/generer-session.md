# Mission : Génération d'un Flux de Travail de Session (`generer-session.md`)

## 1. Objectif
Produire un fichier de flux opérationnel de session (`flux-travail/sessions/flux-travail-s{N}.md`) conforme aux standards pédagogiques N3 et aux règles de gouvernance inter-skills ([regles-flux-sessions.md](../../../rules/regles-flux-sessions.md)).

---

## 2. Entrées Requises
- **Source Concepteur :** Intentions pédagogiques issues de `Sessions/S{N}.md` (compétences mobilisées, objectifs du sprint).
- **Référentiel Universel :** `flux-travail/flux-travail-generique.md` (25 étapes universelles d'ingénierie logicielle).
- **Projet d'Imitation :** Spécifications fonctionnelles et techniques du *Blog des Lauréats* pour le sprint ciblé.

---

## 3. Démarche de Conception et Découpage

1. **Identifier les domaines de compétences mobilisés :**
   - Extraire les domaines techniques et méthodologiques introduits dans la session (ex : `D.325.1-ia`, `D.311.2-uml`, `D.312.1-architecture`, `D.321.1-laravel`).
   - Consolider toutes les notions d'un même domaine dans un **unique UA-Lab** par session.

2. **Déterminer la typologie de chaque phase :**
   - **Phase de type `UA-Lab` :**
     - S'applique dès qu'un domaine de compétence doit être assimilé par l'apprenant.
     - Structurer la phase en deux étapes consécutives :
       1. `Étape : Apprentissage` (notions fondamentales, concepts clés et livrable d'atelier sous `tutoriels/`).
       2. `Étape : Application sur le Blog` (mise en œuvre concrète sur le Blog des Lauréats, en reprenant l'intitulé générique exact du flux universel).
   - **Phase de type `UA-Tâche` :**
     - S'applique lorsque la phase regroupe des activités opérationnelles de gestion de projet, de tests ou de clôture sans nouvel apport théorique.
     - Structurer la phase exclusivement avec des étapes d'application opérationnelle reprenant les intitulés génériques exacts.

3. **Ordonnancement chronologique strict :**
   - Positionner impérativement chaque phase `UA-Lab` immédiatement avant l'étape de réalisation du Blog qui mobilise ce domaine.
   - Respecter le cycle de sprint : Planification & Git $\to$ Phases techniques (UA-Lab avec Apprentissage puis Application Blog) $\to$ Piste Discovery N+1 $\to$ Clôture et Qualité.

4. **Intégrer le Cadre Tri-Projets :**
   - Dans l'étape de réalisation principale du sprint (piste Delivery), expliciter les 3 volets :
     - *Projet d'Imitation (Jours 1 à 7) :* Réalisation guidée pas-à-pas sur le Blog des Lauréats.
     - *Projet Technique (Jour 8) :* Codage pur en autonomie sur le portfolio personnel, sanctionné par le Live Coding de 40 min chrono sans assistance.
     - *Projet Fil Rouge (Jours 9 et 10) :* Création d'un Skill agentique automatisant la tâche sur une application métier.

5. **Spécificités du Sprint 0 (Cadrage et Socle Initial) :**
   - *Prérequis bloquants :* Intégrer les validations du `lab-product-owner` pour le Groupe 1 et du `lab-scrum-master` pour l'ensemble des apprenants.
   - *Initialisation Git :* Création du dépôt Git local et distant (`README.md`) au lieu de la création d'une branche `sprint-N`.
   - *Double unité Laravel 13 :* Découper l'acquisition du socle en deux temps :
     1. Installation de stack, Tailwind CSS, Preline UI et route Hello World Blade.
     2. Démarrage rapide avec le composant TodoList connecté à MySQL pour prononcer le jalon Go/No-Go lors de la Review 0.

---

## 4. Règles de Rédaction Impératives
- **Zéro tableau Markdown (`| ... |` interdit) :** Utiliser exclusivement des listes à puces directes (`- `).
- **Zéro code numérique `UA.*` :** Identifier par `UA-Lab : [Titre] (Domaine D.xxx.x)` ou `UA-Tâche : [Titre]`.
- **Un seul livrable principal unique par étape :** Indiqué sous `Sortie (1 seul livrable) : [chemin]`.
- **Intitulés génériques stricts :** Ne jamais inventer de nom d'étape de réalisation différent du flux générique.
- **Stack technique :** Laravel 13, MySQL exclusivement, Preline UI avec Tailwind CSS, Alpine.js.
