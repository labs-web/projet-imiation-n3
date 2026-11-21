---
name: conception-session
description: >-
  Conçoit, découpe et génère les flux de travail génériques par session de formation
  (flux-travail/sessions/) en Unités d'Apprentissage ordonnées (UA-Lab vs UA-Tâche)
  à partir du flux générique d'ingénierie logicielle et des intentions pédagogiques du concepteur.
---

# Skill Conception de Session : /conception-session

## 1. Mission
Générer et actualiser les flux opérationnels de formation (`flux-travail/sessions/flux-travail-s{N}.md`) pour chaque sprint de 80h.
Le skill applique des règles génériques de structuration de session, indépendantes des spécificités des domaines de compétences (qui sont gouvernées par leurs skills de domaine respectifs).

## 2. Déclenchement
- **Quand l'activer** :
  - Création ou restructuration d'une session de formation (`flux-travail-s{N}.md`).
  - Découpage direct d'un sprint de formation en séquence ordonnée d'Unités d'Apprentissage (`UA-Lab` vs `UA-Tâche`).
  - Audit de conformité structurelle d'une session de formation.
- **Quand NE PAS l'activer** :
  - Découpage didactique interne d'une UA-Lab en tutoriels progressifs -> utiliser `conception-ua-lab`.
  - Modification du flux d'ingénierie universel (`flux-travail-generique.md`) -> utiliser `flux-travail`.
  - Rédaction détaillée des tutoriels d'autoformation -> utiliser `realisation-ua-lab`.
  - Cérémonies de fin de sprint -> utiliser `cloture-sprint`.

## 3. Missions disponibles
L'agent identifie le travail demandé par le concepteur et exécute la mission correspondante située dans `missions/` :
- missions/generer-session.md : Découpe et génère un flux de session en Unités d'Apprentissage ordonnées (`UA-Lab` vs `UA-Tâche`) selon les règles génériques.
- missions/auditer-session.md : Contrôle la conformité d'une session (titrage centré sur l'incrément, typologie des UAs, zéro tableau, statut des tutoriels).

## 4. Règles Génériques Canoniques de Structuration de Session
- **Titrage centré sur l'Incrément :** Le titre officiel du sprint et de la session doit impérativement désigner l'incrément concret produit (ex : *Maquette de la Page d'Accueil*).
- **Proscription des Conteneurs « Phases » :** Chaque session est directement découpée selon une séquence ordonnée d'Unités d'Apprentissage :
  - **`UA-Lab` (Maturité `ua-lab`)** : Dédiées exclusivement à l'assimilation théorique et aux ateliers d'apprentissage guidés. Le découpage didactique atomique est délégué au skill `conception-ua-lab`. Aucune tâche d'application directe sur le projet n'est mélangée aux ateliers d'apprentissage.
  - **`UA-Tâche` (Maturité `projet`)** : Rattachées obligatoirement au domaine de compétence **`D.351.2-realisation-projet`**. Elles regroupent l'ensemble des tâches d'application opérationnelle sur le projet, d'initialisation technique et de rituels agiles.
- **Titrage Canonique Générique des UAs :** Le titre d'une Unité d'Apprentissage ne doit jamais contenir de cas d'usage ou d'application support (ex : Todo List proscrit dans le titre d'une UA).
- **Indication Systématique du Statut de Réalisation :** Chaque tutoriel ou étape d'ingénierie doit obligatoirement mentionner son statut explicite : **`Réalisé`** (avec référence au code `UA.*` officiel le cas échéant) ou **`À réaliser`**.
- **Prérequis Spécifiques de Session :** Les organisations de promotion (sas de mise à niveau, groupes de priorité) doivent être spécifiées dans la section des prérequis de la session concernée.
