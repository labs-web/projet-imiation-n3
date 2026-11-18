---
name: skills-dev
description: >-
  Gouverne, conçoit, crée et raffine les skills, missions et règles du workspace.
  En appel sans consigne, audite les remarques du concepteur non supportées par défaut
  et propose un plan d'évolution sous forme d'artefact.
---

# Skill Méta-Gouvernance : /skills-dev

## 1. Mission
Gouverner, concevoir, créer, auditer et raffiner les **Skills** (`.agents/skills/`), les **Missions** (`missions/`) et les **Règles permanentes** (`.agents/rules/`).
- **Invocation sans argument** : Auditer la discussion récente, extraire les remarques du concepteur non supportées par défaut, et soumettre un plan sous format artefact interactif (`RequestFeedback: true`) avant toute modification.
- **Invocation avec consigne** : Créer ou affiner chirurgicalement une compétence ou une règle.
- **Principes cardinaux** : SSOT (autorité unique), DRY (zéro duplication rules vs skills) et compacité strictly <= 75 lignes.

## 2. Déclenchement
- **Quand l'activer** :
  - Sans argument : Audit réflexif des remarques du concepteur et génération du plan interactif.
  - Avec consigne : Création, refonte ou affinement chirurgical d'un skill ou d'une règle.
  - Contrôle qualité : Compacité (<= 75 lignes), zéro tableau Markdown, liens relatifs purs.
- **Quand NE PAS l'activer** :
  - Réalisation technique applicative directe (utiliser le skill métier dédié).

## 3. Contraintes & Règles Inviolables
- **1. Gating par Artefact Obligatoire** : Appel sans consigne = interdiction d'éditer directement les fichiers. Émettre un plan interactif (`RequestFeedback: true`) et attendre l'accord explicite.
- **2. Arbitrage Règle Transverse vs Skill** : Toute exigence transversale s'applique obligatoirement dans `.agents/rules/` (Always-On), jamais isolée dans un skill.
- **3. Zéro Tableau Markdown** : Règle stricte du projet (utiliser exclusivement des listes à puces `- `).
- **4. Plafond de Compacité** : Tout fichier `SKILL.md` doit respecter strictement <= 75 lignes.
- **5. Portabilité Universelle Pure** : 100% de liens relatifs (`./`, `../`). Aucun lien absolu (`C:`, `D:`, `file:///`).
- **6. Vocabulaire Solicode** : Français A1, termes techniques des développeurs, usage exclusif du mot **Mission**.

## 4. Procédure d'Intervention Pas-à-Pas

### Parcours A : Appel Sans Consigne (Audit Réflexif Concepteur)
- **1. Extraction** : Relever chronologiquement les remarques et rectifications du concepteur dans le chat.
- **2. Diagnostic** : Évaluer si chaque point est supporté par défaut ou révèle une carence documentaire.
- **3. Arbitrage** : Règle transverse -> `.agents/rules/` ; geste technique spécialisé -> `.agents/skills/<nom>/`.
- **4. Artefact de Plan** : Générer `plan.md` (`RequestFeedback: true`) et attendre la validation explicite.
- **5. Application** : Après accord formel, appliquer les modifications chirurgicales.

### Parcours B : Création ou Raffinement avec consigne (`/skills-dev [action]`)
- **1. Cadrage** : Définir la responsabilité unique du skill ou de la règle.
- **2. Rédaction** : Rédiger le fichier en respectant le format standard et les contraintes (<= 75 lignes).
- **3. Contrôle qualité** : Vérifier l'absence de tableaux Markdown et la validité des liens relatifs.
