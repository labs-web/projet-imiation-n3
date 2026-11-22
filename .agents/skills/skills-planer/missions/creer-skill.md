# Mission : Création ou Extension Physique d'un Skill (`creer-skill.md`)

## 1. Contexte & Rôle
Cette mission matérialise physiquement dans le workspace la décision validée par le concepteur : création d'un nouveau skill ou ajout d'une mission dans un skill existant, conformément aux normes canoniques.

---

## 2. Procédure Pas-à-Pas

1. **Cas A : Création d'un Nouveau Skill :**
   - Créer le dossier racine : `.agents/skills/[nom-skill]/`.
   - Créer le sous-dossier des missions : `.agents/skills/[nom-skill]/missions/`.
   - Rédiger le fichier canonique `SKILL.md` (frontmatter YAML, mission, déclenchement, missions disponibles, $\le 75$ lignes).
   - Rédiger chaque fichier `missions/<nom>.md` (contexte, étapes du flux couvertes, entrées/sorties, procédure).
   - Indexer le nouveau skill dans `.agents/README.md`.

2. **Cas B : Ajout d'une Mission dans un Skill Existant :**
   - Rédiger le fichier de la nouvelle mission sous `.agents/skills/[nom-skill]/missions/[nom-mission].md`.
   - Mettre à jour la section `## 3. Missions Disponibles` du `SKILL.md` existant pour déclarer la nouvelle mission.
   - S'assurer que le fichier `SKILL.md` reste $\le 75$ lignes.

3. **Cas C : Reconception de Skills :**
   - Réorganiser les dossiers et missions selon le plan validé.
   - Mettre à jour `.agents/README.md` et les références associées.
