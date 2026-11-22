# Mission : Couverture et Création de Compétence Pré-Étape (`couvrir-etape-sprint.md`)

## 1. Contexte & Rôle
Cette mission est obligatoirement convoquée par `realisation-sprint` **avant chaque réalisation d'étape de flux**.
Elle prend en charge :
1. La critique systématique du plan préliminaire (`docs/plan-preliminaire-skills.md`).
2. La conception et la création physique immédiate du skill ou de la mission manquant.
3. La présentation sous artéfact interactif pour validation formelle par le concepteur avant exécution de l'étape.

---

## 2. Procédure Pas-à-Pas

1. **Audit de l'Étape & Critique du Plan Préliminaire :**
   - Identifier l'étape à réaliser et son livrable unique.
   - Examiner ce qui avait été projeté dans `docs/plan-preliminaire-skills.md`.
   - Critiquer la prévision initiale : identifier ses manques ou limites face au travail réel et formuler une organisation supérieure.

2. **Conception & Création Physique Immédiate :**
   - Définir le skill et ses missions (rappel : une mission peut couvrir plusieurs étapes).
   - Exécuter immédiatement la création physique des fichiers (`SKILL.md` $\le 75$ lignes et fichiers `missions/*.md`).

3. **Soumission de l'Artéfact de Validation au Concepteur :**
   - Émettre l'artéfact interactif de validation (`validation-skill-[nom].md` avec `RequestFeedback: true`).
   - Présenter au concepteur :
     - La compétence créée et ses fichiers sources prêts.
     - La critique du plan préliminaire et la justification de la solution adoptée.
     - L'étape du flux débloquée par ce skill.
   - Attendre l'approbation formelle (*Proceed*) du concepteur.

4. **Feu Vert d'Exécution :**
   - Dès validation, donner le feu vert à `realisation-sprint` pour exécuter l'étape avec son skill officiel.
