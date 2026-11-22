# Règle : Affichage Systématique des Skills Utilisés

Ce document définit la règle obligatoire régissant l'affichage des compétences spécialisées (skills) mobilisées par l'Agent IA lors de ses échanges avec l'utilisateur.

---

## 1. Obligation Systématique en Fin d'Échange

- À la fin de chaque message, réponse ou interaction avec l'utilisateur, l'Agent IA doit obligatoirement inclure un bloc récapitulant les compétences (skills) mobilisées lors du traitement de la demande.
- Si un ou plusieurs skills spécialisés ont été mobilisés, l'Agent IA doit citer leur nom canonique ainsi qu'une brève justification de leur rôle ou de la mission exécutée.
- Si aucun skill spécialisé n'a été invoqué et que l'Agent IA s'est appuyé uniquement sur le socle des règles permanentes, la mention doit l'expliciter clairement.

---

## 2. Format Canonique Obligatoire

Le bloc doit être inséré tout en bas de la réponse, immédiatement après une ligne de séparation horizontale (`---`) :

```markdown
---
**Skills utilisés :** `[nom-du-skill-1]` (justification concise ou mission exécutée), `[nom-du-skill-2]` (justification concise)
```

Exemple en cas de réponse sans recours à un skill spécialisé :
```markdown
---
**Skills utilisés :** Aucun skill spécifique (application directe du socle de règles permanentes `.agents/rules/`).
```

---

## 3. Champ d'Application

Cette règle est transversale et intangible :
- Elle s'applique à tous les agents et personas opérant dans le workspace (`realisation-sprint`, sous-agents, etc.).
- Elle s'applique à toutes les interactions de développement, de conception, d'audit ou de planification.
