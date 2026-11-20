# Registre de Synchronisation Inter-Agents (`.sync/`)

Ce dossier est l'espace pivot de synchronisation et de gouvernance de versions entre l'**Agent Projet** (`projet-imiation-n3`) et l'**Agent Autoformation** (`autoformations-professionaliser`).

---

## 1. Rôle du dossier `.sync/` pour le Concepteur

Le dossier `.sync/` centralise la coordination technique entre les deux agents sans polluer les dossiers de code et de livrables :
- **Point de vérité des versions** : Il stocke l'arborescence miroir contenant exclusivement les fichiers `version.yml`.
- **Passerelle inter-agents** : Il permet à l'Agent Autoformation d'auditer l'état réel des livrables produits par l'Agent Projet afin d'alimenter les parcours de formation Jekyll.
- **Découplage** : Les dossiers applicatifs (`tutoriels/`, `rapport/`, `src/`) restent vierges de tout fichier de configuration de synchronisation interne.

---

## 2. Skills Utilisés par chaque Agent

Seuls les skills suivants interagissent avec l'espace `.sync/` :

- **Agent Projet (`projet-imiation-n3`)** :
  - `realisation-ua-lab` : Produit les livrables dans `tutoriels/`, initialise et incrémente leurs versions dans `.sync/.../version.yml`, et notifie le tutoriel source.
  - `cloture-sprint` : Contrôle la présence et la conformité des fichiers `version.yml` lors des rituels de fin de sprint.
- **Agent Autoformation (`autoformations-professionaliser`)** :
  - `tutorial-lab-writer` : Consulte `.sync/` pour récupérer le code réel et les diagrammes à injecter dans les cours Jekyll.
  - `session-flux-travail-adapter` : Analyse `.sync/` pour aligner les sessions de formation sur la réalité des livrables du projet.

---

## 3. Missions Réalisées par chaque Agent

### Missions de l'Agent Projet :
- **Gestion du versioning miroir** : Initialiser et incrémenter les versions sémantiques dans `.sync/` pour chaque livrable ou fichier de code créé ou modifié.
- **Notification de réalisation** : Mettre à jour le front-matter du tutoriel source dans `_tutos/` avec le sprint actif, le statut et la liste des livrables associés avec leurs versions.

### Missions de l'Agent Autoformation :
- **Audit des versions** : Vérifier dans `.sync/` la disponibilité et la version courante des livrables du projet d'imitation.
- **Intégration pédagogique** : Extraire les artefacts concrets (code source, présentations Marp) pour enrichir les fiches de cours Jekyll et acter la synchronisation.
- **Adaptation mutuelle** : Réajuster les consignes ou la théorie du tutoriel source lorsque le projet d'imitation valide une solution technique plus adaptée.

---

## 4. Documentation Associée

Pour le détail des règles et du processus pas-à-pas, consulter :
- [rules.md](./rules.md) : Contrat officiel des règles partagées et du système de versioning.
- [workflow-tuto.md](../docs/workflow-tuto.md) : Guide du cycle de vie des tutoriels, format des fichiers `version.yml` et valeurs du workflow `statut_realisation`.
