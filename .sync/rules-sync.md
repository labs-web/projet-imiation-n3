# Règles Partagées de Synchronisation Inter-Agents (rules-sync.md)

Ce document définit les règles normatives de synchronisation et de versioning entre l'Agent Projet (`projet-imiation-n3`) et l'Agent Autoformation (`autoformations-professionaliser`).

---

## 1. Primauté Normative des Règles de Livrables

> [!IMPORTANT]
> **Souveraineté Normative de l'Agent Autoformation :**  
> L'Agent Autoformation est l'autorité normative qui définit de façon stricte la structure, le formatage et l'arborescence de tous les livrables du cursus.  
> - **Livrables d'apprentissage (fiches, présentations, commandes) :** Logés impérativement sous `tutoriels/[slug-domaine]/[slug-ua]/[slug-tuto]/[slug-tuto].md`, `presentation-[slug-tuto].md`, `[slug-tuto].command.md` (aucun `README.md` unitaire).  
> - **Livrables opérationnels de projet (UA-Tâche) :** Logés sous les répertoires officiels (`README.md`, `sprints/`, `scrum/`, `docs/cadrage/`, `docs/analyse/`, `docs/produit/`, `docs/design/`).  
> **L'Agent Projet s'adapte obligatoirement à cette nomenclature canonique et ne peut inventer d'arborescences divergentes.**

---

## 2. Rôles et Responsabilités

- **Agent Projet (`projet-imiation-n3`)** :
  - Développe le code applicatif, produit les artéfacts opérationnels et les livrables attendus sous `docs/`, `sprints/`, `scrum/` et `tutoriels/` selon la nomenclature imposée par l'Agent Autoformation.
  - Maintient l'arborescence miroir des versions exclusivement dans le dossier `.sync/`.
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