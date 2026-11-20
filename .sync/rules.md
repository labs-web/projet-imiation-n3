# Règles Partagées de Synchronisation Inter-Agents

Ce document définit les règles de synchronisation et de versioning entre l'Agent Projet (`projet-imiation-n3`) et l'Agent Autoformation (`autoformations-professionaliser`).

---

## 1. Rôles et Responsabilités

- **Agent Projet** :
  - Réalise les fonctionnalités du sprint, rédige les fiches techniques, produit les diaporamas Marp et développe le code.
  - Maintient l'arborescence miroir des versions exclusivement dans le dossier `.sync/`.
  - Notifie la réalisation d'un tutoriel en mettant à jour le front-matter du tutoriel source avec le sprint, le statut de réalisation et la liste des livrables associés avec leurs versions.
- **Agent Autoformation** :
  - Rédige et maintient le catalogue des tutoriels sources dans `_tutos/`.
  - Consulte `.sync/` dans le projet d'imitation pour identifier les livrables existants et leurs versions courantes.
  - Compare les numéros de version déclarés dans le front-matter avec ceux de `.sync/` pour détecter les mises à jour et synchroniser le contenu réel (code, diagrammes) dans les parcours de formation Jekyll.

---

## 2. Système de Versioning dans `.sync/`

- **Emplacement strict dans `.sync/`** :
  - Les fichiers `version.yml` existent **exclusivement à l'intérieur du dossier `.sync/`**.
  - Il est formellement interdit de créer des fichiers `version.yml` dans les dossiers applicatifs (`tutoriels/`, `rapport/`, `src/`).
- **Création systématique et obligatoire** :
  - Un fichier `version.yml` doit être créé pour chaque sous-dossier contenant des livrables existants ou des fichiers de code existants ou modifiés.
- **Format ultra-minimaliste** :
  - Correspondance directe entre le nom du fichier et son numéro de version sémantique :
    ```yaml
    nom-du-fichier.md: "1.0.0"
    presentation-nom-du-fichier.md: "1.0.0"
    ```
- **Incrémentation continue** :
  - À chaque passage de l'Agent IA modifiant un fichier existant, la version du fichier est obligatoirement incrémentée (`1.0.0` -> `1.0.1` pour un correctif, `1.1.0` pour un enrichissement).

---

## 3. Traçabilité et Synchronisation dans le Front-Matter du Tutoriel Source

L'Agent Projet met à jour le front-matter du tutoriel source dans `_tutos/` avec un bloc minimaliste :

```yaml
sprint: "sprint1"
statut_realisation: "realise"
livrables:
  - chemin: "tutoriels/scrum/initiation-scrum/comprendre-scrum/comprendre-scrum.md"
    version: "1.0.0"
  - chemin: "tutoriels/scrum/initiation-scrum/comprendre-scrum/presentation-comprendre-scrum.md"
    version: "1.0.0"
```

- **Rôle des champs** :
  - `sprint` : Nom du sprint de réalisation (ex: `sprint1`).
  - `statut_realisation` : État d'avancement du tutoriel dans le workflow (ex: `realise`, `synchronise`, `a_adapter`).
  - `livrables` : Liste libre des livrables produits ou utilisés pour ce tutoriel (fiches, présentations Marp, code, scripts), associant chaque `chemin` relatif à sa `version` utilisée.
- **Mécanisme de synchronisation basé sur les versions** :
  - L'Agent Autoformation compare la version déclarée dans le front-matter (`version: "1.0.0"`) avec la version courante inscrite dans `.sync/.../version.yml`.
  - Si la version de `.sync/` est supérieure à celle du front-matter, l'Agent Autoformation détecte une mise à jour, actualise les extraits de code et diagrammes dans Jekyll, aligne la version dans le front-matter et passe le statut à `synchronise`.

---

## 4. Principe d'Adaptation Mutuelle

- **Cas 1 : Livrable incomplet ou décalé par rapport au tutoriel source** :
  - L'Agent Projet adapte le livrable dans `tutoriels/` pour satisfaire tous les critères attendus.
- **Cas 2 : Évolution technique du projet (mise à jour Laravel, architecture 2 couches)** :
  - Si le projet réel valide une solution plus pertinente que la consigne initiale, l'Agent Autoformation met à jour le tutoriel de référence dans `_tutos/` pour aligner la théorie sur la pratique.
