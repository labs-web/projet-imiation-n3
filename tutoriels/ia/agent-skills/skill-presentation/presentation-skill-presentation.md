---
marp: true
theme: default
paginate: true
header: "Solicode N3 - Tutoriel 3 (Atelier) : Skill Presentation"
footer: "Encadrant : ESSARRAJ Fouad | Solicode Tanger"
---

<!-- _class: lead -->
# Conception d'un Skill Agentique
### Tutoriel 3 (Atelier) — Exemple `skill-presentation`

- **Apprenant** : Apprenant Solicode
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Domaine** : Ingénierie de prompt et agents IA (ia)
- **Compétence** : c-325 — Concevoir des Agents IA et développer des Skills
- **Date** : 2026-11-18

---

## 1. Objectifs de l'Atelier
- Expérimenter la conception d'un skill modulaire pour Agent IA.
- Appliquer la structure canonique normalisée (plafond <= 75 lignes).
- Pratiquer l'encapsulation de missions opératoires dans missions/.
- Valider la découvrabilité native par le frontmatter YAML.

---

## 2. Anatomie d'un Skill Modulaire
- **Fichier SKILL.md (Routeur)** :
  - Frontmatter YAML avec name et description précise.
  - Définition de la mission générale en 1-2 phrases.
  - Critères de déclenchement (quand l'activer / quand ne pas l'activer).
  - Catalogue des missions disponibles.
- **Dossier missions/** :
  - Découpage des tâches opératoires spécifiques.

---

## 3. Le Skill d'Exemple : skill-presentation
- **Mission** : Orchestrer la création de présentations orales.
- **Mission encapsulée** : missions/marp-slides.md.
  - Génération de diapositives au format Marp Markdown.
  - Page de garde réglementaire Solicode Tanger.
  - Zéro tableau Markdown (listes à puces exclusives).

---

## 4. Application sur le Projet d'Imitation
- Modèle appliqué directement sur le projet Blog des lauréats :
  - Skill skills-dev pour la méta-gouvernance.
  - Skill gestion-depot (24 lignes) avec ses 2 missions :
    - missions/init-depot.md (Git local, branche, GitHub CLI).
    - missions/init-projet.md (README.md, arborescence racine).

---

<!-- _class: lead -->
# Conclusion de l'Atelier
### Modularité & Compacité Maîtrisées
- Validation pratique de la compétence c-325.
- Architecture robuste prête pour l'industrialisation des agents.
