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
   - Extraire les domaines techniques et méthodologiques introduits dans la session (ex : `D.311.1-design`, `D.311.2-uml`, `D.312.1-architecture`, `D.321.1-laravel`).
   - Consolider toutes les notions d'un même domaine dans un **unique UA-Lab** par session.

2. **Déterminer la séquence directe des Unités d'Apprentissage :**
   - Proscrire tout conteneur de « Phase » englobant. Le flux opérationnel est constitué directement par la suite ordonnée des Unités d'Apprentissage.
   - **Unités d'Apprentissage de type `UA-Lab` (Maturité `ua-lab`) :**
     - S'applique dès qu'un domaine de compétence doit être assimilé par l'apprenant.
     - Structurer l'UA-Lab en étapes normées :
       1. `Étape : Tutoriel-lab : [Intitulé]` (notions fondamentales et atelier guidé). Produit **obligatoirement 2 livrables** : un guide explicatif (`guide-[nom].md`) et une présentation Marp (`presentation-[nom].md`).
       2. `Étape : Tutoriel-application : [Intitulé]` (mise en œuvre concrète sur le Blog des Lauréats). Ne fait partie du UA-Lab que si c'est une application directe de l'atelier du lab.
   - **Unités d'Apprentissage de type `UA-Tâche` (Maturité `projet`, 3 blocs au maximum par session) :**
     - S'applique lorsque le bloc regroupe des activités opérationnelles de gestion de projet, de cadrage, de tests ou de clôture sans nouvel apport théorique (rattachées à `D.351.2-realisation-projet`).
     - Structurer la session autour de 3 blocs d'UA-Tâches au maximum :
       1. *UA-Tâche Début :* Lancement, planification et initialisation de l'environnement (Git, README).
       2. *UA-Tâche Milieu :* Tâches transverses de modélisation, de backlog ou de préparation Discovery.
       3. *UA-Tâche Fin :* Rituels de clôture, Qualité DoD, Sprint Review et Sprint Retrospective.

3. **Ordonnancement chronologique et rédaction :**
   - Positionner impérativement chaque `UA-Lab` immédiatement avant l'étape de réalisation du Blog qui mobilise ce domaine.
   - **Titres épurés :** Ne jamais insérer la mention de l'étape générique dans le titre de l'étape (`### Étape X : [Titre]`).
   - **Traçabilité en description :** Indiquer la référence générique au début du corps : `- Correspondance flux générique : Étape Générique N (...)`.

4. **Intégrer le Cadre Tri-Projets :**
   - Dans l'étape de réalisation principale du sprint (piste Delivery), expliciter les 3 volets :
     - *Projet d'Imitation :* Réalisation guidée pas-à-pas sur le Blog des Lauréats.
     - *Projet Technique :* Codage pur en autonomie sur le portfolio personnel lors des sprints de delivery (Live Coding sommative).
     - *Projet Fil Rouge :* Développement applicatif métier pur (sans agents IA).

5. **Spécificités du Sprint 0 (Cadrage et Backlog Initial — Sans Code) :**
   - *Aucun code dans S0 :* Ni Laravel 13, ni MySQL, ni architecture logicielle MVC (déplacés en Session S1).
   - *Organisation promotion :* Le formateur constitue 5 groupes d'apprentissage hiérarchisés par priorité et présente formellement le Groupe 1 comme Product Owner.
   - *Initialisation Git :* Création du dépôt Git local et distant (`README.md`) au lieu de la création d'une branche `sprint-N`.
   - *Durées indicatives :* Les 80 heures et 10 jours sont purement indicatifs.

---

## 4. Règles de Rédaction Impératives
- **Zéro tableau Markdown (`| ... |` interdit) :** Utiliser exclusivement des listes à puces directes (`- `).
- **Titrage canonique générique des UAs :** Identifier par `UA.[code] (UA-Lab) : [Titre canonique générique]` (sans cas d'usage) ou `UA.[code] (UA-Tâche) : [Titre]`.
- **Intitulés génériques stricts dans le corps de texte.**
- **Stack technique :** Laravel 13, MySQL exclusivement, Preline UI avec Tailwind CSS, Alpine.js.
