---
name: skills-dev
description: >-
  Gouverne, conçoit, crée et raffine les skills, missions et règles du workspace.
  En appel sans consigne, audite les remarques du concepteur non supportées par défaut
  et propose un plan d'évolution sous forme d'artefact.
---

# Skill Méta-Gouvernance : /skills-dev

## 1. Mission
Gouverner, concevoir, créer, auditer et raffiner les **Skills** (`.agents/skills/`), leurs **Missions** (`<skill>/missions/<nom>.md`) et les **Règles permanentes** (`.agents/rules/`).
- **Invocation sans argument** : Auditer la discussion récente, extraire les remarques du concepteur non supportées par défaut, et soumettre un plan sous format artefact interactif (`RequestFeedback: true`) avant toute modification.
- **Invocation avec consigne ou étape** : Analyser l'étape du flux de travail (`flux-travail.md`) et proposer soit l'ajout d'une mission dans un skill existant (`<skill>/missions/<nom>.md`), soit la création d'un nouveau skill.
- **Principes cardinaux** : SSOT (autorité unique), DRY (zéro duplication rules vs skills) et compacité strictly <= 75 lignes.

## 2. Déclenchement
- **Quand l'activer** :
  - Sans argument : Audit réflexif des remarques du concepteur et génération du plan interactif.
  - Avec consigne ou étape de flux : Analyse d'étape, création de nouveau skill ou ajout d'une mission encapsulée.
  - Contrôle qualité : Compacité (<= 75 lignes), zéro tableau Markdown, liens relatifs purs.
- **Quand NE PAS l'activer** :
  - Réalisation technique applicative directe (utiliser le skill métier dédié).

## 3. Contraintes & Règles Inviolables
- **1. Gating par Artefact Obligatoire** : Appel sans consigne = interdiction d'éditer directement les fichiers. Émettre un plan interactif (`RequestFeedback: true`) et attendre l'accord explicite.
- **2. Arbitrage Règle Transverse vs Skill** : Toute exigence transversale s'applique obligatoirement dans `.agents/rules/` (Always-On), jamais isolée dans un skill.
- **3. Zéro Tableau Markdown** : Règle stricte du projet (utiliser exclusivement des listes à puces `- `).
- **4. Plafond de Compacité** : Tout fichier `SKILL.md` doit respecter strictement <= 75 lignes.
- **5. Portabilité Universelle Pure** : 100% de liens relatifs (`./`, `../`). Aucun lien absolu (`C:`, `D:`, `file:///`).
- **6. Encapsulation des Missions** : Chaque mission est stockée dans `<skill>/missions/<nom>.md` (sans suffixe `.mission.md`).

## 4. Procédure d'Intervention Pas-à-Pas

### Parcours A : Appel Sans Consigne (Audit Réflexif Concepteur)
- **1. Extraction** : Relever chronologiquement les remarques et rectifications du concepteur dans le chat.
- **2. Diagnostic** : Évaluer si chaque point est supporté par défaut ou révèle une carence documentaire.
- **3. Arbitrage** : Règle transverse -> `.agents/rules/` ; compétence ciblée -> `.agents/skills/<nom>/`.
- **4. Artefact de Plan** : Générer `plan.md` (`RequestFeedback: true`) et attendre la validation explicite.
- **5. Application** : Après accord formel, appliquer les modifications chirurgicales.

### Parcours B : Traitement d'Étape ou Consigne (`/skills-dev [étape | consigne]`)
- **1. Analyse** : Analyser les tâches de l'étape de flux ou la consigne demandée.
- **2. Décision** : Déterminer si la tâche s'intègre comme mission dans un skill existant (`<skill>/missions/<nom>.md`) ou justifie un nouveau skill (`.agents/skills/<nom>/SKILL.md`).
- **3. Rédaction & Validation** : Rédiger le fichier en respectant le format standard et les contraintes (<= 75 lignes).
