# Flux de travail du projet

Ce document formalise les étapes de réalisation du Projet d'imitation Niveau 3. Il sert de référentiel méthodologique pour guider l'apprenant et l'Agent IA dans la production des livrables.

Les projets suivent les démarches d'ingénierie logicielle : 2TUP, Design Thinking, modélisation UML et méthodologie Agile/Scrum.

La planification des sprints et l'identification du sprint actif sont centralisées dans [sprints/sprints.md](../sprints/sprints.md).

---

# Sprint 1

Les objectifs détaillés et le déroulement du sprint sont définis dans [sprints/sprints.md](../sprints/sprints.md).

---

## 1. Création et initialisation du projet

### Base théorique et pratique
- Installation et utilisation de GitHub CLI (`gh repo create`).
- Création et gestion des branches Git (`sprint[N]`).

### Prérequis
- Présentation et cadrage du projet d'imitation par le formateur référent.

### Travail à faire
- **Tâche 1 : Initialisation locale** : Créer le projet, initialiser Git (`git init`) et réaliser le premier commit.
- **Tâche 2 : Publication sur GitHub** : Créer la branche `sprint1` et publier le dépôt via GitHub CLI avec la commande : `gh repo create`.
- **Tâche 3 : Rédaction du README.md** : Nettoyer et structurer le fichier `README.md` racine selon le template standard Solicode en intégrant la stack technique (Laravel 12).

### Livrables
- Dépôt GitHub distant publié et synchronisé sur la branche `sprint1`.
- Fichier `README.md` propre et conforme.
- Planification Scrum : `sprints/sprints.md` et `sprints/README.md`.
- Skill outillé : `.agents/skills/gestion-depot/` (avec sa mission `missions/init-projet.md`).

---

## 2. Initialisation de l'Agent IA

### Base théorique et pratique
- Formulation de consignes, rôles et règles IA.
- Architecture d'un agent outillé (règles et skills).

### Prérequis
- Dépôt Git initialisé et publié sur GitHub sur la branche `sprint1` (Étape 1).

### Travail à faire
- Définir le socle commun des règles et contexte du projet : `.agents/rules/contexte-projet.md` et `.agents/rules/regles-generales.md`.
- Mettre en place les skills initiaux dans `.agents/skills/` (`skills-dev`, `gestion-depot`, `flux-travail`, `marp`, `realisation-ua-lab`).
- Configurer l'environnement agentique pour la découverte native des skills.

### Livrables
- Règles permanentes : `.agents/rules/contexte-projet.md`, `.agents/rules/regles-generales.md`.
- Skills agentiques configurés dans `.agents/skills/`.

---

## 3. Documentation du Flux de Travail

### Base théorique et pratique
- Démarche 2TUP, ingénierie logicielle et formalisation des étapes.

### Prérequis
- Initialisation de l'Agent IA terminée (Étape 2).

### Travail à faire
- Initialiser le document de suivi du flux de travail : `flux-travail/flux-travail.md`.
- Formaliser la structure standardisée des étapes (`Base théorique et pratique`, `Prérequis`, `Travail à faire`, `Livrables`).
- Mettre en place le skill de gouvernance du flux : `.agents/skills/flux-travail/SKILL.md`.
- Rédiger le guide du dossier : `flux-travail/README.md`.

### Livrables
- Fichier `flux-travail/flux-travail.md`.
- Skill outillé : `.agents/skills/flux-travail/SKILL.md`.
- Guide pédagogique : `flux-travail/README.md`.

---

## 4. Cadrage du projet sous gouvernance Scrum

### Base théorique et pratique
- Piliers Scrum, rôles d'équipe et formalisation du sprint.

### Prérequis
- Documentation du flux de travail initialisée (Étape 3).

### Travail à faire
- Formaliser le fichier de planification des sprints : `sprints/sprints.md`.
- Définir le Sprint 1 en statut Actif avec ses objectifs et sa branche Git `sprint1`.
- Rédiger le guide du dossier : `sprints/README.md`.

### Livrables
- Fichier de cadrage Scrum : `sprints/sprints.md`.
- Guide méthodologique : `sprints/README.md`.
- Branche Git `sprint1` synchronisée.

---

## 5. Structuration du Product Backlog et des issues

### Base théorique et pratique
- Découpage en user stories, priorisation et gestion du backlog.

### Prérequis
- Cadrage Scrum du Sprint 1 formalisé (Étape 4).

### Travail à faire
- Créer l'espace de suivi des tâches du projet : dossier `issues/`.
- Recenser les user stories et tâches du Sprint 1 issues du Product Backlog.
- Organiser les issues par statut (`issues-open.md`, `issues-à-valider.md`, `issues-closes.md`).
- Soumettre les issues à la validation du formateur avant dépôt sur GitHub.

### Livrables
- Guide pédagogique : `issues/README.md`.
- Fichiers de suivi des tâches : `issues/issues-open.md`, `issues/issues-à-valider.md`, `issues/issues-closes.md`.

---

## 6. Modélisation du contexte et des cas d'utilisation avec Mermaid

### Base théorique et pratique
- Modélisation UML textuelle avec la syntaxe Mermaid (diagramme de contexte, cas d'utilisation).

### Prérequis
- User stories et tâches du Sprint 1 recensées dans `issues/` (Étape 5).

### Travail à faire
- Modéliser le diagramme de contexte du système (utilisateurs lauréats, apprenants, système de publication).
- Modéliser le diagramme de cas d'utilisation pour la consultation des articles.
- Déposer les diagrammes dans `docs/modelisation/`.

### Livrables
- Guide du dossier : `docs/README.md`.
- Fiches de modélisation Mermaid : `docs/modelisation/contexte.md` et `docs/modelisation/cas-utilisation.md`.

---

## 7. Conception de l'architecture logicielle en 2 couches

### Base théorique et pratique
- Séparation des responsabilités, contrôleurs minces et classes Services.

### Prérequis
- Modélisation des cas d'utilisation validée (Étape 6).

### Travail à faire
- Définir le pattern architectural en 2 couches : `ArticleController` (Contrôleur mince) vers `ArticleService` (Classe Service).
- Spécifier les signatures des méthodes métier pour la récupération d'un article.
- Documenter le principe d'architecture dans `docs/architecture/`.

### Livrables
- Documentation de l'architecture logicielle : `docs/architecture/architecture-2-couches.md`.

---

## 8. Implémentation sous Laravel 12 de la consultation d'un article

### Base théorique et pratique
- Routage Laravel 12, injection de service, gabarit Blade responsive et gestion d'erreur HTTP 404.

### Prérequis
- Conception de l'architecture 2 couches validée (Étape 7).

### Travail à faire
- Configurer la route de consultation d'un article dans Laravel 12.
- Implémenter le contrôleur mince `ArticleController` injectant `ArticleService`.
- Développer la classe `ArticleService` pour la logique de récupération des données d'article.
- Gérer explicitement l'exception de ressource introuvable avec renvoi d'une erreur 404 propre.
- Créer le gabarit Blade responsive pour l'affichage détaillé de l'article.
- Vérifier manuellement le bon affichage responsive et le comportement en cas d'article inexistant.

### Livrables
- Code source Laravel 12 : Route, Contrôleur mince, Classe Service et vue Blade responsive.
- Gestion fonctionnelle de l'erreur 404.
- Page de consultation détaillée d'un article opérationnelle.
