# Règles Partagées de Synchronisation Inter-Agents (rules-sync.md)

Ce document définit les règles normatives de synchronisation et de versioning entre l'Agent Projet (`projet-imiation-n3`) et l'Agent Autoformation (`autoformations-professionaliser`).

---

## 1. Primauté Normative des Règles de Livrables

> [!IMPORTANT]
> **Souveraineté Normative de l'Agent Autoformation :**  
> L'Agent Autoformation est l'autorité normative qui définit de façon stricte la structure, le formatage et l'arborescence de tous les livrables du cursus à travers les documents de référence normatifs colocalisés :  
> - `.agents/rules/persona.md` (identité officielle de l'**Agent Réalisation de Sprint**)  
> - `.agents/references/organisation-livrables.md` (arborescence universelle du poste apprenant)  
> - `.agents/references/typologie-uas-tutoriels.md` (catégories d'UAs et slugs des tutoriels)  
> - `.agents/references/gitflow.md` (stratégie des branches et conventions de commits)  
> - **Livrables d'apprentissage (`tuto-lab`, `tuto-notion`, `tuto-code`) :** Logés impérativement sous `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/` (seul `tutoriels/README.md` existe, aucun `README.md` unitaire).  
> - **Livrables opérationnels de projet (`tuto-tache`) :** Logés sous les répertoires officiels (`README.md`, `sprints/`, `scrum/`, `docs/cadrage/`, `docs/analyse/`, `docs/produit/`, `docs/conception/`). Aucun journal CLI `.command.md` requis.  
> **L'Agent Réalisation de Sprint s'adapte obligatoirement à cette nomenclature canonique et ne peut inventer d'arborescences divergentes.**

---

## 2. Rôles et Responsabilités

- **Agent Réalisation de Sprint (`realisation-sprint`, projet cible)** :
  - Incarne l'apprenant type de Solicode qui suit la formation (tous niveaux N1, N2, N3).
  - Développe le code applicatif (`src/`), produit les artéfacts opérationnels et les livrables attendus selon la nomenclature imposée par l'Agent Autoformation.
  - Maintient l'arborescence miroir des versions exclusivement dans le dossier `.sync/`.
  - Ne committe ni ne pousse jamais de façon autonome (souveraineté de l'apprenant).
  - Notifie la réalisation d'un tutoriel dans le front-matter du tutoriel source (`_tutos/`) avec le statut `realise` et la liste des livrables et versions.
- **Agent Autoformation (`autoformations-professionaliser`)** :
  - Conçoit le cadre didactique (`_sessions/`, `_uas/`, `_tutos/`).
  - Audite le dossier `.sync/` du projet d'imitation, compare les numéros de version déclarés et synchronise le contenu réel vers Jekyll en basculant le statut à `synchronise`.

---

## 3. Système de Versioning dans `.sync/`

- **Emplacement strict dans `.sync/`** :
  - Les fichiers `version.yml` existent **exclusivement à l'intérieur du dossier `.sync/`**.
  - Interdiction stricte de créer des fichiers `version.yml` dans `tutoriels/`, `docs/`, `src/`.
- **Création systématique** :
  - Un fichier `version.yml` pour chaque dossier contenant des livrables.
- **Format sémantique minimaliste** :
  ```yaml
  nom-du-fichier.md: "1.0.0"
  presentation-nom-du-fichier.md: "1.0.0"
  ```
- **Incrémentation continue** :
  - `1.0.0` -> `1.0.1` pour un correctif, `1.1.0` pour un enrichissement.

---

## 4. Traçabilité dans le Front-Matter du Tutoriel Source

```yaml
sprint: "sprint0"
statut_realisation: "realise"
livrables:
  - chemin: "tutoriels/scrum/initiation-scrum/comprendre-scrum/comprendre-scrum.md"
    version: "1.0.0"
  - chemin: "tutoriels/scrum/initiation-scrum/comprendre-scrum/presentation-comprendre-scrum.md"
    version: "1.0.0"
```

---

## 5. Principe d'Adaptation Mutuelle

- Si un livrable est incomplet ou décalé, l'Agent Projet adapte son fichier pour respecter les standards édictés par l'Agent Autoformation.
- Si le projet réel valide une amélioration technique pertinente, l'Agent Autoformation met à jour le tutoriel de référence dans `_tutos/`.