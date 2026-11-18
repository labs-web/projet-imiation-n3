---
marp: true
theme: default
paginate: true
header: "Solicode — N3 Développer / Réaliser | Skill Clôture de Sprint"
footer: "Architecture des Skills IA & Rituels Scrum | Sprint 1"
---

<!-- _class: lead -->
# Skill Modulaire : Clôture de Sprint
## Orchestration IA des 4 rituels de fin de sprint
**Apprenant :** Équipe de Développement N3  
**Encadrant :** ESSARRAJ Fouad  
**Établissement :** Solicode Tanger  
**Domaine :** D.351.2 — Réalisation de projet | **Compétence :** C.325 & C.351  
**Date :** Novembre 2026

---

# 1. Problématique & Évolution Didactique
- Les prompts isolés (`*.prompt.md`) sont passifs et manuels
- Risque de dispersion des fichiers dans l'arborescence
- Manque de contrôle sur le contexte chargé par l'Agent IA
- Solution moderne : Concevoir un **Agent Skill modulaire** unifié
- Déclenchement automatique par commande `/cloture-sprint`

---

# 2. Architecture Modulaire du Skill
- Orchestrateur racine compact dans `SKILL.md` (plafond $\le 75$ lignes)
- Définition sémantique des conditions d'activation et d'exclusion
- Répartition en 4 sous-missions spécialisées dans `missions/`
- Documentation complète pour l'équipe dans `doc/how-to-use.md`
- Isolation stricte des contextes pour chaque rituel

---

# 3. Les 4 Missions Orchestrées
- **Sprint Review :** Démonstration live & audit binaire DoD (7 critères)
- **Sprint Retrospective :** Forces, freins & dette d'empathie utilisateur
- **Backlog Refinement :** Archivage des issues & réordonnancement S2
- **Débriefing Session :** Auto-évaluation C.311-C.351 & bilan Live Coding
- Sorties directes sous `scrum/` et `issues/` sans tableau Markdown

---

# 4. Bénéfices pour le Projet Fil Rouge
- Réutilisabilité intégrale sur les sprints futurs (S2, S3, S4)
- Gain de temps majeur lors de chaque clôture de cycle
- Garantie de conformité méthodologique pour chaque livrable
- Entraînement concret à l'ingénierie avancée des Agents IA
- Capitalisation pérenne dans le patrimoine d'outillage de l'équipe
