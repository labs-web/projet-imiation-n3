---
version: "1.0.0"
description: "Échelle de maturité didactique EFP (veille, lab, ua-lab, tutoriel, projet) et cycle de maturation pour l'intégration de labs au référentiel."
---

# Référentiel Normatif : Échelle de Maturité EFP & Cycle de Maturation Lab ➔ UA-Lab

## 1. Principes & Séparation Hermétique : Maturité vs Typologie

L'ingénierie didactique de l'**EFP (Établissement de Formation Professionnelle)** repose sur une dissociation absolue entre la **Maturité** et la **Typologie** :

- **Dimension `maturite` :**
  - Question clé : *À quel stade d'évolution et de validation dans le cursus EFP se trouve ce contenu ?*
  - Rôle pédagogique : Niveau d'ancrage institutionnel et de validation sur le terrain.
  - Slugs officiels EFP : `veille`, `lab`, `ua-lab`, `tutoriel`, `projet`.
- **Dimension `type` :**
  - Question clé : *Quelle est la structure physique et la nature de ce document didactique ?*
  - Rôle pédagogique : Gabarit, livrables attendus, exigences Marp et CLI.
  - Slugs officiels EFP : `tuto-atelier`, `tuto-notion`, `tuto-code`, `tuto-tache`.

> [!IMPORTANT]
> **Règle Inviolable de Dissociation des Slugs :**
> - Les slugs de maturité et les slugs de type sont **strictement distincts**.
> - Les types de tutoriels adoptent tous le préfixe unifié **`tuto-*`** (`tuto-atelier`, `tuto-notion`, `tuto-code`, `tuto-tache`).
> - Le format d'atelier guidé s'intitule **`tuto-atelier`**. Il est formellement distinct des maturités **`lab`** et **`ua-lab`**.

---

## 2. L'Échelle de Maturité de l'EFP

$$\text{veille} \longrightarrow \text{lab} \longrightarrow \text{ua-lab} \longrightarrow \text{tutoriel} \quad (+\; \text{projet})$$

1. **`veille` :** Recherche exploratoire, prospective technique, identification de nouvelles technologies ou approches sans atelier structuré.
2. **`lab` :** Atelier d'expérimentation pratique guidé. L'apprenant est mis en posture de recherche active. **On ne donne PAS les notions de base en détail**, mais uniquement le travail à faire, les compétences à acquérir et les pistes de recherche.
3. **`ua-lab` :** **Un Lab réalisé, validé sur le terrain par les apprenants, puis officiellement intégré dans le référentiel de compétences de l'EFP**. À ce stade, le plan de l'UA-Lab est formellement spécifié et **les notions de base sont données en détail** (cours théorique de référence consolidé).
4. **`tutoriel` :** Industrialisation didactique complète (découpage déterministe $E_{n-1} \to E_n$, code incrémental autonome).
5. **`projet` :** Dimension transverse d'ingénierie opérationnelle (cadrage, Product Backlog, rituels Scrum, revues et rétrospectives, **0% théorie**).

---

## 3. Matrice de Correspondance Maturité et Typologie

- **Maturité `lab` $\times$ Typologie `tuto-atelier` :**
  - Atelier pratique guidé en recherche active : **SANS notions de base en détail**.
  - Livrables attendus : Diaporama Marp (`presentation-[slug].md`) + Fiche de restitution (`[slug].md`) + Journal CLI (`[slug].command.md` si CLI) sous `tutoriels/`.
- **Maturité `ua-lab` $\times$ Typologie `tuto-atelier` :**
  - Lab **validé et intégré au référentiel EFP** : Plan d'UA spécifié + **Notions de base DONNÉES EN DÉTAIL** (« Notions fondamentales » consolidées).
  - Même structure de livrables sous `tutoriels/`.
- **Maturité `tutoriel` $\times$ Typologie `tuto-notion` :**
  - Concepts théoriques et notions isolées hors projet d'imitation (sous `tutoriels/`, sans Marp, rapport CLI si manipulation).
- **Maturité `tutoriel` $\times$ Typologie `tuto-code` :**
  - Progression incrémentale $E_{n-1} \to E_n$ sur le projet d'imitation (code sous `src/`, sans Marp, rapport CLI sous `tutoriels/`).
- **Maturité `projet` $\times$ Typologie `tuto-tache` :**
  - Tâches de projet opérationnelles et rituels Scrum (0% théorie, fichiers racine `docs/`, `sprints/`, `scrum/`, sans Marp, sans CLI).

---

## 4. Cycle de Maturation d'un Atelier : `lab` $\longrightarrow$ `ua-lab`

Un document de type **`tuto-atelier`** traverse obligatoirement 3 phases séquentielles :

```mermaid
sequenceDiagram
    participant Redacteur as Agent Rédacteur (Autoformation)
    participant Jekyll as Plateforme EFP (Jekyll)
    participant Apprenant as Agent Réalisation (Projet Cible)
    participant Sync as Registre .sync/

    Note over Redacteur,Jekyll: Phase 1 : Publication en maturité 'lab'
    Redacteur->>Jekyll: Fiche maturite: "lab", type: "tuto-atelier" (SANS notions détaillées)
    
    Note over Jekyll,Apprenant: Phase 2 : Réalisation & Recherche active
    Apprenant->>Apprenant: Recherche active, expérimentation, Marp, commandes CLI
    Apprenant->>Apprenant: Produit les livrables dans tutoriels/
    Apprenant->>Sync: Déclare version.yml (statut: realise)

    Note over Sync,Redacteur: Phase 3 : Validation & Intégration Référentiel EFP
    Sync-->>Redacteur: Notification de réalisation
    Redacteur->>Redacteur: Audit des livrables réels de l'apprenant
    Redacteur->>Redacteur: Spécifie formellement le plan de l'UA-Lab
    Redacteur->>Redacteur: Rédige les notions de base EN DÉTAIL
    Redacteur->>Jekyll: Met à jour vers maturite: "ua-lab", statut: "synchronise"
```

### Phase 1 : Maturité `lab` (Avant Réalisation — Recherche Active)
L'Agent Rédacteur conçoit le cadre de l'atelier sans prémâcher le travail :
- **Frontmatter Jekyll :**
  ```yaml
  maturite: "lab"
  type: "tuto-atelier"
  statut_realisation: "a_realiser"
  ```
- **Structure Markdown :**
  - Contexte & Enjeux : Pourquoi cette compétence est requise dans le sprint.
  - Ce que vous devez apprendre : Objectifs pédagogiques clairs, problématiques à explorer.
  - Travail à faire : Consignes directives sur les livrables à concevoir et tester.
  - Pistes de recherche active : Questions directrices guidant l'investigation sans donner la solution.
  - Livrables attendus :
    - Fiche d'atelier : `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/[slug-tuto].md`
    - Diaporama Marp : `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/presentation-[slug-tuto].md`
    - Journal CLI : `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/[slug-tuto].command.md` (si CLI)
  - ⚠️ **ZÉRO section « Notions fondamentales » détaillée à cette étape.**

---

### Phase 2 : Réalisation par l'Agent Réalisation de Sprint (`realisation-sprint`)
- L'apprenant prend en charge la fiche en maturité `lab`.
- Il mène l'investigation, produit sa synthèse dans `tutoriels/.../[slug].md`, son diaporama Marp et son journal CLI.
- Il met à jour `.sync/.../version.yml` et notifie `statut_realisation: "realise"`.

---

### Phase 3 : Maturité `ua-lab` (Lab Validé & Intégré au Référentiel de Compétences EFP)
- **Déclencheur :** Notification `statut_realisation: "realise"`.
- **Frontmatter Jekyll :**
  ```yaml
  maturite: "ua-lab"
  type: "tuto-atelier"
  statut_realisation: "synchronise"
  ```
- **Enrichissements apportés par l'Agent Rédacteur :**
  - Audit des livrables : Vérification de la véracité technique et de la qualité du support Marp.
  - Spécification du Plan de l'UA-Lab : Structuration formelle de la fiche UA dans `_uas/` (articulation des tâches, alignement sur les compétences certifiantes `C.xxx`).
  - Notions de base données en détail : Rédaction de la section **« Notions fondamentales »** : cours théorique rigoureux et synthétique (les 20% discriminants vérifiés sur le terrain).
  - Conservation des pistes d'approfondissement dans « Recherches à effectuer ».
