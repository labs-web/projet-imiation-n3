---
marp: true
theme: default
paginate: true
header: "Solicode N3 - Tutoriel 2 : Architecture Agent IA"
footer: "Encadrant : ESSARRAJ Fouad | Solicode Tanger"
---

<!-- _class: lead -->
# Architecture d'un Agent IA et Règles Always-On
### Tutoriel 2 — Unité d'Apprentissage UA.325.11

- **Apprenant** : Apprenant Solicode
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Domaine** : Ingénierie de prompt et agents IA (ia)
- **Compétence** : c-325 — Concevoir des Agents IA et développer des Skills
- **Date** : 2026-11-18

---

## 1. Paliers d'Autonomie : LLM vs Chatbot vs Agent
- **LLM** : Moteur statistique sans état, isolé du système.
- **Chatbot** : Interface de dialogue passive, sans accès aux fichiers.
- **Agent IA** : Entité autonome dotée d'outils et de perception.
  - Cycle : Perception du workspace -> Raisonnement -> Action outillée.

---

## 2. Outils & Environnement Augmenté
- **Accès aux fichiers** : Manipulation de fichiers via des chemins relatifs.
- **Boîte à outils de l'agent** :
  - Outil terminal (`run_command`) pour la compilation et les tests.
  - Outils de lecture (`read_file`, `list_dir`) pour l'inspection.
  - Outils d'écriture (`write_file`, `edit_file`) pour les modifications ciblées.

---

## 3. Architecture : Rules Always-On vs Skills
- **Rules (.agents/rules/)** :
  - Directives permanentes chargées à chaque interaction.
  - Cadre inviolable : zéro tableau, liens relatifs, non-commit par l'IA.
- **Skills (.agents/skills/)** :
  - Compétences modulaires activées à la demande.
  - Plafond strict de compacité (<= 75 lignes).
  - Découvrabilité native par frontmatter YAML.

---

## 4. Principes SSOT & DRY
- **SSOT (Single Source of Truth)** :
  - Une seule autorité par règle pour éviter les divergences.
- **DRY (Don't Repeat Yourself)** :
  - Aucune répétition des règles générales dans les skills.
- **Gouvernance Humaine** :
  - Validation, commit et push strictement réservés au concepteur.

---

<!-- _class: lead -->
# Conclusion du Tutoriel 2
### Socle de l'Agent IA Maîtrisé
- Architecture solide alliant règles Always-On et compétences modulaires.
- Prêt pour l'atelier pratique : Conception du skill d'exemple skill-presentation.
