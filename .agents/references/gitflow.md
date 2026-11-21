---
version: "1.0.0"
description: "Norme de gestion des versions sous Git, stratégie des branches par sprint, conventions de commits atomiques et souveraineté exclusive de l'apprenant."
---

# Stratégie GitFlow et Conventions de Commits

## 1. Principes Fondamentaux de Gestion de Version

Ce document définit les règles de gestion de version sous Git appliquées sur le poste de l'apprenant et par l'**`Agent Réalisation de Sprint`** :
- La stratégie des branches par sprint.
- L'interdiction formelle du travail direct sur la branche principale (`main`).
- La souveraineté exclusive de l'apprenant sur les actions de commit et de push.
- Les conventions de nommage des commits atomiques.

---

## 2. Stratégie des Branches par Sprint

1. **Branche Dédiée au Sprint Actif :**
   - L'ensemble des activités d'un sprint (cadrage, tutoriels, code applicatif, documentation) s'effectue sur la branche unique dédiée :
     - Sprint 0 : `sprint0`
     - Sprint 1 : `sprint1`
     - Sprint N : `sprintN`
2. **Interdiction Formelle de Travailler sur `main` :**
   - La branche `main` est protégée. Aucun travail de développement en cours ne doit y être réalisé directement.
   - La fusion vers `main` n'intervient qu'en clôture de sprint, après validation formelle de la Sprint Review et obtention de la décision Go.
3. **Création et Basculement de Branche :**
   - Vérifier la branche courante : `git branch --show-current`
   - Créer et basculer sur la branche du sprint actif : `git checkout -b sprint[N]`

---

## 3. Souveraineté de l'Apprenant & Interdiction IA

> [!CAUTION]
> **Règle Absolue :**  
> L'Agent IA a l'**interdiction formelle** d'exécuter de sa propre initiative les commandes `git commit` et `git push`.  
> L'apprenant conserve l'entière maîtrise de son historique de versioning. L'agent prépare les fichiers, les organise et informe l'apprenant qu'ils sont prêts à être inspectés et committés.

---

## 4. Conventions de Commits Atomiques

Les messages de commit doivent respecter le format standard Conventional Commits :
- `feat(cadrage): formaliser la note de cadrage et le perimetre in/out`
- `feat(tuto-scrum): realiser le tutoriel comprendre-scrum et sa presentation marp`
- `feat(conception): creer les maquettes de la page d accueil sous preline ui`
- `fix(routes): corriger le routage des articles de blog`
- `docs(sprint0): formaliser le proces-verbal de review et la retrospective`
