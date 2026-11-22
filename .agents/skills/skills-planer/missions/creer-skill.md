# Mission : Création ou Extension Physique d'un Skill (`creer-skill.md`)

## 1. Contexte & Rôle
Cette mission matérialise physiquement dans le workspace la décision validée par le concepteur : création d'un nouveau skill ou ajout d'une mission dans un skill existant, conformément aux normes canoniques.

---

## 2. Procédure Pas-à-Pas

1. **Cas A : Création d'un Nouveau Skill :**
   - Créer le dossier racine : `.agents/skills/[nom-skill]/`.
   - Créer le sous-dossier des missions : `.agents/skills/[nom-skill]/missions/`.
   - Rédiger le fichier canonique `SKILL.md` (frontmatter YAML, mission, déclenchement, missions disponibles, $\le 75$ lignes).
   - Rédiger chaque fichier `missions/<nom>.md` (contexte, étapes couvertes, entrées/sorties, procédure normative).
   - Indexer le nouveau skill dans `.agents/README.md`.

2. **Cas B : Ajout d'une Mission dans un Skill Existant :**
   - Rédiger le fichier de la nouvelle mission sous `.agents/skills/[nom-skill]/missions/[nom-mission].md`.
   - Mettre à jour la section `## 3. Missions Disponibles` du `SKILL.md` existant pour déclarer la nouvelle mission.
   - S'assurer que le fichier `SKILL.md` reste $\le 75$ lignes.

3. **Cas C : Reconception de Skills :**
   - Réorganiser les dossiers et missions selon le plan validé.
   - Mettre à jour `.agents/README.md` et les références associées.

---

## 3. Checklist Obligatoire de Généricité & Autonomie
Avant de finaliser tout fichier de compétence (`SKILL.md` ou mission) :
- **100% Générique :** Le contenu ne contient aucun nom de projet spécifique en dur, aucune entité métier figée (ex: pas d'hypothèse rigide sur le *Blog*). Il s'applique à tout projet web.
- **Zéro Dépendance Didactique :** Aucune référence à des tutoriels, des labs d'apprentissage, ou des dossiers `tutoriels/` / `ua-lab/`. Le skill est taillé pour un projet réel d'entreprise.
- **Découplage Méthode / Données :** Le skill porte la méthode d'ingénierie et la structure attendue ; les données réelles sont instanciées à l'exécution depuis le contexte projet.
- **Règles Techniques :** Zéro tableau Markdown, liens relatifs obligatoires, style A1/A2 direct.
