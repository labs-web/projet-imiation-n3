# Règles Partagées de Synchronisation Inter-Agents

Ce document définit les règles communes entre l'Agent Projet (`projet-imiation-n3`) et l'Agent Autoformation (`autoformations-professionaliser`).

---

## 1. Rôles et Responsabilités

- **Agent Projet** :
  - Réalise les fonctionnalités du sprint, rédige les fiches techniques, produit les diaporamas Marp et développe le code.
  - Maintient l'arborescence miroir des versions dans `.sync/`.
  - Notifie la réalisation d'un tutoriel en mettant à jour le front-matter du tutoriel source.
- **Agent Autoformation** :
  - Rédige et maintient le catalogue des tutoriels sources dans `_tutos/`.
  - Consulte `.sync/` dans le projet d'imitation pour identifier les fichiers concrets utilisables.
  - Référence et intègre les fichiers de code et les diagrammes réels dans les parcours de formation Jekyll.

---

## 2. Normes des Livrables

- **Format sans tableau** :
  - Interdiction absolue des tableaux Markdown (`| ... |`).
  - Utilisation exclusive de listes à puces directes (`- `).
- **Langue et niveau rédactionnel** :
  - Niveau de français A1 : phrases courtes, claires et actives (Sujet + Verbe + Complément).
  - Utilisation du vocabulaire technique professionnel (ex: *commit, branch, sprint, contrôleur, service, Blade, route*).
- **Liens relatifs obligatoires** :
  - Interdiction des chemins absolus (`C:\...`, `D:\...`) et des liens `file:///`.
  - Tous les liens doivent être relatifs et portables sur GitHub.
- **Présentations Marp** :
  - Format Marp Markdown strict.
  - Page de garde obligatoire avec le logo Solicode, la compétence, le domaine et le formateur référent ESSARRAJ Fouad.

---

## 3. Système de Versioning dans `.sync/`

- **Emplacement du dossier miroir** :
  - Dossier racine `.sync/` qui réplique les chemins des sous-dossiers modifiés.
- **Règle de création sélective** :
  - Un fichier `version.yml` est créé uniquement dans les sous-dossiers contenant des fichiers modifiés lors de la réalisation du sprint.
- **Format ultra-minimaliste** :
  - Uniquement la correspondance directe entre le nom du fichier et son numéro de version sémantique :
    ```yaml
    nom-du-fichier.md: "1.0.0"
    presentation-nom-du-fichier.md: "1.0.0"
    ```
- **Incrémentation continue** :
  - À chaque passage de l'Agent IA modifiant un fichier existant, la version du fichier est obligatoirement incrémentée.

---

## 4. Traçabilité dans le Front-Matter du Tutoriel Source

L'Agent Projet met à jour le front-matter du tutoriel dans `_tutos/` avec les métadonnées suivantes :

```yaml
realise_dans_sprint: true
sprint: "sprint1"
statut_realisation: "realise"
etape_workflow: "valide"
date_realisation: "YYYY-MM-DD"
```

---

## 5. Principe d'Adaptation Mutuelle

- **Cas 1 : Livrable incomplet ou décalé par rapport au tutoriel source** :
  - L'Agent Projet adapte le livrable dans `tutoriels/` pour satisfaire tous les critères attendus.
- **Cas 2 : Évolution technique du projet (mise à jour Laravel, architecture 2 couches)** :
  - Si le projet réel valide une solution plus pertinente que la consigne initiale, l'Agent Autoformation met à jour le tutoriel de référence dans `_tutos/` pour aligner la théorie sur la pratique.
