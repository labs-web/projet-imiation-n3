# Mission : Audit de Conformité d'une Session (`auditer-session.md`)

## 1. Objectif
Vérifier la conformité d'un flux opérationnel de session (`flux-travail/sessions/flux-travail-s{N}.md`) avec les standards pédagogiques N3 et les règles de gouvernance ([regles-flux-sessions.md](../../../rules/regles-flux-sessions.md)).

---

## 2. Checklist d'Audit Pédagogique

1. **Fiche d'identification et Cadre Tri-Projets :**
   - La durée est-elle strictement fixée à 80 heures (10 jours) ?
   - Les trois volets sont-ils explicites : Projet d'Imitation (J1-7), Projet Technique (J8 avec épreuve de Live Coding 40 min en codage pur sans conception), et Projet Fil Rouge (J9-10 avec Skills agentiques) ?

2. **Typologie stricte des Phases (`UA-Lab` vs `UA-Tâche`) :**
   - Chaque phase est-elle formellement typée `UA-Lab` ou `UA-Tâche` ?
   - Toute phase `UA-Lab` comprend-elle bien une `Étape : Apprentissage` immédiatement suivie d'une `Étape : Application sur le Blog` ?
   - Les phases `UA-Tâche` regroupent-elles exclusivement des activités opérationnelles sans théorie superflue ?

3. **Précédence temporelle de l'apprentissage :**
   - Chaque phase `UA-Lab` précède-t-elle la première tâche du Blog qui en a besoin ?
   - Les notions d'un même domaine sont-elles consolidées dans un unique UA-Lab par session ?

4. **Fidélité nominale au Flux Générique :**
   - Toutes les étapes d'application reprennent-elles l'intitulé exact de l'étape générique correspondante dans `flux-travail/flux-travail-generique.md` ?
   - Chaque étape de session produit-elle un seul livrable principal unique ?

5. **Interdictions formelles et standards de formatage :**
   - Aucun tableau Markdown (`| ... |` proscrit) : uniquement des listes à puces directes (`- `).
   - Aucun code numérique hardcodé (`UA.*` proscrit).
   - Aucun framework ou SGBD obsolète : MySQL et Laravel 13 obligatoires.
   - Stack conforme : Laravel 13, MySQL exclusivement, Preline UI et Tailwind CSS.
