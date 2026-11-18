---
name: marp
description: >-
  Génère des présentations de diapositives au format Marp Markdown avec page de garde
  normalisée (apprenant, encadrant, établissement, domaine, compétence) et sans aucun tableau Markdown.
---

# Skill Présentation : /marp

## 1. Mission
Concevoir des présentations pédagogiques et interactives au format Marp Markdown (`*.md`) pour restituer les apprentissages théoriques et pratiques des UA-Labs.

## 2. En-tête YAML obligatoire
Chaque fichier de présentation doit démarrer par ce bloc de configuration :

```yaml
---
marp: true
theme: default
paginate: true
header: "Solicode N3 - [slug-domaine]"
footer: "Encadrant : ESSARRAJ Fouad | Solicode Tanger"
---
```

## 3. Page de garde normalisée (Slide 1)
La première diapositive doit impérativement adopter cette disposition :

```markdown
<!-- _class: lead -->
# [Titre du Laboratoire]
### [Sous-titre / Thème de l'UA-Lab]

- **Apprenant** : [Nom de l'apprenant]
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Domaine** : [slug-domaine]
- **Compétence** : [Code & Nom de la compétence]
- **Date** : [Date du jour]
```

## 4. Règles de conception des diapositives
- **Séparateur de diapositive** : Utiliser `---` sur une ligne dédiée pour changer de diapositive.
- **Règle zéro tableau Markdown** : Interdiction formelle des tableaux. Présenter l'information avec des listes à puces (`- `), des blocs de citation (`> `) ou du code.
- **Densité** : 1 idée majeure par diapositive, 4 à 6 puces claires au maximum.
- **Style et langue** : Français A1 direct, phrases courtes (Sujet + Verbe + Complément) et vocabulaire professionnel de développeur.
- **Diapositive de conclusion** : Toujours conclure par un récapitulatif des acquis clés et un échange de questions/réponses.
- **Liens relatifs** : Utiliser exclusivement des liens relatifs pour les ressources référencées.
