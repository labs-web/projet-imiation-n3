# Mission : Validation et Clôture de Jalon (`valider-jalon.md`)

## 1. Contexte & Rôle
Cette mission intervient lorsque l'ensemble des étapes d'un jalon ont été exécutées. Elle formalise la revue du jalon et sollicite la validation formelle du concepteur avant d'autoriser la transition vers le jalon suivant.

---

## 2. Procédure Pas-à-Pas

1. **Audit de Complétude des Livrables du Jalon :**
   - Vérifier la présence physique et la non-régression de l'ensemble des livrables attendus pour le jalon.
   - S'assurer de la conformité aux critères d'acceptation opérationnels.

2. **Génération de l'Artéfact de Bilan de Jalon :**
   - Émettre un artéfact interactif standardisé (`bilan-jalon-[N]-[id].md` avec `RequestFeedback: true`).
   - Présenter de manière épurée :
     - La liste des étapes exécutées et leurs livrables associés (liens relatifs).
     - Les choix techniques et arbitrages majeurs effectués.
     - Les points d'attention ou recommandations pour le jalon suivant.

3. **Attente de Validation Formelle :**
   - Inviter le concepteur à tester ou relire les livrables et à cliquer sur *Proceed* pour débloquer le jalon suivant.
   - Prendre en compte tout commentaire ou ajustement demandé avant de basculer.
