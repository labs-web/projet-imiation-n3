# Planification des Sprints

Ce document enregistre les sprints du projet. Les sprints suivants seront ajoutés ultérieurement, après chaque session de planification. Pour le moment, seul le Sprint 1 est actif avec la description détaillée du sprint actuel ci-dessous.

---

## Sprint 1 : Initialisation, Cadrage & Première Fonctionnalité Laravel 12
- **Statut** : Actif
- **Branche Git** : `sprint1`
- **Vision du produit** : Le *Blog des Lauréats* est une vitrine web conçue pour valoriser publiquement les réalisations et profils techniques des lauréats de Solicode auprès des recruteurs et des apprenants.
- **Acteurs cibles** :
  - *Acteur primaire (Consommateur en S1)* : L'Apprenant ou le Visiteur/Recruteur, qui souhaite consulter le catalogue des réalisations et lire en détail chaque article publié.
  - *Acteur secondaire (Contributeur)* : Le Lauréat, qui soumettra et administrera ses articles dans un sprint ultérieur.
- **Périmètre du Sprint 1** :
  - *In-Scope (Strictement inclus dans le Sprint 1)* :
    - Consultation publique de la fiche détaillée d'un article de blog via sa route dynamique `/articles/{id}`.
    - Architecture logicielle découplée en deux couches : Contrôleur mince HTTP -> Classe Service.
    - Stockage tabulaire transitoire en mémoire à partir d'un fichier CSV (`articles.csv`).
    - Rendu responsive sous gabarit Blade avec layout maître et composants d'interface.
    - Gestion résiliente de l'erreur HTTP 404 en cas d'identifiant d'article inexistant.
  - *Out-of-Scope (Strictement exclu du Sprint 1)* :
    - Zéro module d'authentification ou de connexion utilisateur.
    - Zéro formulaire de rédaction, modification ou suppression d'article.
    - Zéro base de données relationnelle MySQL (reportée aux sprints ultérieurs).
- **Objectif pédagogique** : Au terme de la session, l'apprenant est capable d'initialiser un dépôt distant avec GitHub CLI, d'outiller l'environnement avec un Agent IA et un catalogue de missions, de formaliser le processus de développement et le flux de travail, de cadrer le projet sous gouvernance Scrum, de modéliser le diagramme de contexte et les cas d'utilisation avec Mermaid, de gérer les tâches via le dossier `issues/`, et de développer sous Laravel 12 une page de consultation détaillée d'un article selon une architecture 2 couches (Contrôleur mince -> Classe Service) avec gabarit Blade responsive et gestion de l'erreur 404.
- **Déroulement (Vue d'ensemble du travail de la session)** :
  - Initialiser le projet et publier sur GitHub.
  - Outiller l'environnement avec un Agent IA et son catalogue de missions.
  - Formaliser le flux de travail d'ingénierie.
  - Cadrer le périmètre sous gouvernance Scrum.
  - Modéliser le contexte et les cas d'utilisation avec Mermaid.
  - Structurer le Product Backlog et les issues dans `issues/`.
  - Concevoir l'architecture en 2 couches (Contrôleur mince -> Classe Service).
  - Implémenter la consultation d'un article sous Laravel 12 (gabarit Blade responsive et gestion 404).
