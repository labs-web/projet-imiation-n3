---
name: skill-presentation
description: >-
  Génère des présentations orales et diaporamas pédagogiques.
  Délègue la conception à ses missions spécialisées dans missions/.
---

# Skill Présentation : /skill-presentation

## 1. Mission
Orchestrer la création de présentations de diapositives pour la soutenance de projet et les restitutions d'apprentissage.

## 2. Déclenchement
- **Quand l'activer** :
  - L'apprenant demande la création d'un diaporama de présentation ou d'une soutenance orale.
- **Quand NE PAS l'activer** :
  - Rédaction de documentations textuelles standards (utiliser les skills de documentation).

## 3. Missions disponibles
L'agent identifie le format demandé et exécute la mission correspondante située dans `missions/` :
- `missions/marp-slides.md` : Générer un diaporama au format Marp Markdown avec page de garde normalisée Solicode.
