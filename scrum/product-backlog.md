# Product Backlog : Blog des Lauréats

> Livrable d'ingénierie logicielle — Étape 9 du flux de développement (Cadre Scrum : Product Backlog Initial).

---

## 1. Principes & Règles de Gestion du Product Backlog

Le Product Backlog constitue le référentiel unique et vivant des exigences du projet **Blog des Lauréats**. Il est aligné sur le Product Goal défini dans [docs/produit/vision-produit.md](../docs/produit/vision-produit.md) et répond directement aux besoins identifiés dans [docs/analyse/personas.md](../docs/analyse/personas.md).

### Normes de Rédaction des User Stories (US)
- **Format canonique :** *"En tant que [Persona], je souhaite [Action / Besoin métier] afin de [Bénéfice / Valeur ajoutée]".*
- **Respect strict des critères INVEST :**
  - **I**ndépendante : Chaque US peut être développée et livrée de façon autonome.
  - **N**égociable : Les détails techniques restent ajustables lors de l'affinement.
  - **V**aleur : Chaque US apporte une valeur directe vérifiable à l'utilisateur.
  - **E**stimable : L'effort de développement peut être dimensionné en Story Points (suite de Fibonacci : 1, 2, 3, 5, 8).
  - **S**uffisamment petite : Réalisable au sein d'une seule itération de sprint.
  - **T**estable : Comporte des critères d'acceptation précis et vérifiables.

### Ordonnancement MoSCoW
Le backlog est rigoureusement ordonné selon les 4 niveaux de priorité MoSCoW pour piloter la réalisation par la valeur :
- **Must Have :** Fonctionnalités vitales formant le cœur du Produit Minimum Viable (MVP).
- **Should Have :** Fonctionnalités à forte valeur ajoutée planifiées dès consolidation du socle.
- **Could Have :** Fonctionnalités d'enrichissement et de confort traitées si la vélocité le permet.
- **Won't Have :** Fonctionnalités formellement exclues du périmètre du cycle actif.

---

## 2. Découpage par Épopées Métier (Epics)

Le périmètre applicatif est regroupé en 4 épopées fonctionnelles :
- **Epic 1 : Consultation & Découverte Publique** (Accès aux contenus, lecture fluide, recherche et filtres).
- **Epic 2 : Gestion des Auteurs & Profils** (Inscription, authentification et vitrine professionnelle des lauréats).
- **Epic 3 : Rédaction & Cycle de Vie des Articles** (Création, brouillons, soumission et gestion éditoriale).
- **Epic 4 : Modération Éditoriale & Administration** (Supervision, validation des parutions et gestion des catégories).

---

## 3. Product Backlog Ordonné (Priorisation MoSCoW)

### A. Priorité Must Have (Cœur du MVP — Sprints 0 & 1)

- **US-01 : Consultation de la liste des articles publiés**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite consulter la liste des derniers articles publiés sur la page d'accueil afin de découvrir les nouveaux retours d'expérience disponibles.
  - **Critères d'Acceptation :**
    - Seuls les articles ayant le statut "Publié" sont visibles sur l'interface publique.
    - Chaque carte d'article affiche son titre, sa catégorie, le nom de l'auteur, sa date de parution et un extrait du contenu.
    - La liste est ordonnée par ordre antéchronologique (les plus récents en premier).
    - Une pagination fluide limite l'affichage à 9 articles par page.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 1.

- **US-02 : Lecture d'un article complet**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite accéder à la page détaillée d'un article afin de lire son contenu intégral et ses enseignements professionnels.
  - **Critères d'Acceptation :**
    - La page présente le titre complet, la catégorie, le corps de texte structuré et les informations sur l'auteur.
    - La typographie est optimisée pour une lecture agréable sur mobile et desktop.
    - Un bouton de retour permet de revenir facilement à la liste des articles.
    - Si l'article demandé n'existe pas ou n'est pas publié, une page d'erreur 404 claire s'affiche.
  - **Estimation :** 2 Story Points.
  - **Epic :** Epic 1.

- **US-03 : Filtrage des articles par catégorie thématique**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite filtrer les articles par catégorie (ex: Carrière, Laravel, Insertion) afin de consulter uniquement les sujets correspondant à mes besoins actuels.
  - **Critères d'Acceptation :**
    - Les catégories actives sont affichées sous forme de badges cliquables.
    - Le clic sur une catégorie actualise la liste des articles sans rechargement lourd.
    - Un badge "Tous" permet de réinitialiser le filtre à tout moment.
    - Un message clair s'affiche si aucun article n'est disponible dans la catégorie sélectionnée.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 1.

- **US-04 : Authentification sécurisée des lauréats**
  - **Énoncé :** En tant que Sara (lauréate), je souhaite m'authentifier avec mon adresse email et mon mot de passe afin d'accéder à mon espace de contribution personnel.
  - **Critères d'Acceptation :**
    - Formulaire de connexion avec validation stricte des champs et protection CSRF.
    - Gestion sécurisée des sessions et hachage des mots de passe avec bcrypt.
    - Message d'erreur explicite en cas d'identifiants incorrects sans divulgation d'information sensible.
    - Lien de déconnexion sécurisé accessible depuis le menu utilisateur.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 2.

- **US-05 : Rédaction et enregistrement en brouillon d'un article**
  - **Énoncé :** En tant que Sara (lauréate), je souhaite rédiger un nouvel article et pouvoir le sauvegarder au statut "Brouillon" afin de travailler à mon rythme sans le rendre visible au public.
  - **Critères d'Acceptation :**
    - Formulaire d'édition comprenant : titre, sélection de catégorie, image d'illustration et corps de texte.
    - Bouton d'action "Enregistrer comme brouillon" positionnant le statut de l'article à "Brouillon".
    - L'article au statut brouillon n'apparaît pas dans la liste publique des articles.
    - L'auteur peut retrouver ses brouillons dans son tableau de bord personnel.
  - **Estimation :** 5 Story Points.
  - **Epic :** Epic 3.

- **US-06 : Soumission d'un article pour modération**
  - **Énoncé :** En tant que Sara (lauréate), je souhaite soumettre mon article finalisé à la modération afin qu'il soit relu et validé avant sa publication officielle.
  - **Critères d'Acceptation :**
    - Bouton "Soumettre pour publication" vérifiant que tous les champs obligatoires sont renseignés.
    - Le statut de l'article bascule de "Brouillon" à "En attente de validation".
    - L'article est immédiatement listé dans le tableau de bord des modérateurs.
    - L'auteur ne peut plus modifier l'article tant que la modération n'a pas statué.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 3.

- **US-07 : Modération et publication d'un article soumis**
  - **Énoncé :** En tant que Karim (modérateur), je souhaite examiner les articles en attente et les publier en un clic afin de garantir la qualité éditoriale du blog.
  - **Critères d'Acceptation :**
    - Tableau de bord dédié listant tous les articles au statut "En attente de validation".
    - Vue de prévisualisation conforme au rendu final de l'article.
    - Bouton "Approuver & Publier" basculant le statut à "Publié" avec horodatage de publication.
    - Bouton "Renvoyer pour correction" permettant d'ajouter un commentaire explicatif à l'attention de l'auteur.
  - **Estimation :** 5 Story Points.
  - **Epic :** Epic 4.

- **US-08 : Administration du référentiel des catégories**
  - **Énoncé :** En tant que Karim (administrateur), je souhaite créer, modifier et archiver des catégories afin de structurer les thématiques d'articles du blog.
  - **Critères d'Acceptation :**
    - Interface d'administration sécurisée accessible uniquement aux utilisateurs ayant le rôle "Admin" ou "Modérateur".
    - Création d'une catégorie avec nom unique, slug généré automatiquement et description.
    - Impossibilité de supprimer une catégorie contenant des articles publiés (blocage d'intégrité avec alerte explicative).
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 4.

---

### B. Priorité Should Have (Consolidation & Confort — Sprints Ultérieurs)

- **US-09 : Moteur de recherche textuel sur les articles**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite rechercher des articles par mots-clés dans le titre ou le contenu afin de cibler instantanément une notion technique précise.
  - **Critères d'Acceptation :** Champ de recherche accessible dans l'en-tête, recherche sur titre et corps, surbrillance des termes trouvés.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 1.

- **US-10 : Fiche de profil public de l'auteur lauréat**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite consulter la fiche profil d'un lauréat avec sa biographie et ses liens LinkedIn et GitHub afin d'en apprendre davantage sur son parcours et le contacter.
  - **Critères d'Acceptation :** Page profil affichant nom, photo, biographie, liens sociaux vérifiés et liste de ses articles publiés.
  - **Estimation :** 3 Story Points.
  - **Epic :** Epic 2.

- **US-11 : Estimation automatique du temps de lecture**
  - **Énoncé :** En tant que Youssef (apprenant), je souhaite visualiser le temps moyen de lecture calculé pour chaque article afin d'organiser mon temps de consultation.
  - **Critères d'Acceptation :** Calcul automatique basé sur un ratio standard de 200 mots par minute, affiché sous la forme "X min de lecture" sur la carte et la page détail.
  - **Estimation :** 1 Story Point.
  - **Epic :** Epic 1.

---

### C. Priorité Could Have (Valeur Ajoutée Optionnelle)

- **US-12 : Boutons de partage rapide sur les réseaux sociaux**
  - **Énoncé :** En tant que lecteur, je souhaite partager facilement un article pertinent sur LinkedIn ou Twitter en un clic.
  - **Critères d'Acceptation :** Boutons de partage pré-remplissant l'URL et le titre de l'article sans nécessiter de script externe lourd.
  - **Estimation :** 2 Story Points.
  - **Epic :** Epic 1.

- **US-13 : Statistiques de consultation pour l'auteur**
  - **Énoncé :** En tant que Sara (lauréate), je souhaite visualiser le nombre de vues de mes articles publiés dans mon espace personnel pour mesurer l'impact de mes partages.
  - **Critères d'Acceptation :** Compteur de vues incrémenté lors de chaque consultation unique de la page détail, affiché uniquement sur le tableau de bord de l'auteur.
  - **Estimation :** 2 Story Points.
  - **Epic :** Epic 3.

---

### D. Priorité Won't Have (Exclu Formellement du Cycle Actif)

- **US-14 : Messagerie instantanée en direct entre usagers**
  - **Statut :** Exclu. Les échanges directs s'effectuent via les profils LinkedIn et GitHub des lauréats pour éviter la lourdeur d'une infrastructure de chat temps réel.
- **US-15 : Système d'abonnements payants ou monétisation**
  - **Statut :** Exclu. La plateforme est un service communautaire gratuit sans finalité marchande.
- **US-16 : Application mobile native dédiée**
  - **Statut :** Exclu. L'approche web responsive mobile-first répond à 100% des besoins sans imposer le coût de développement et de maintenance de deux applications natives (iOS/Android).

---

## 4. Définition de Terminé (Definition of Done - DoD) de Référence

Pour qu'une User Story soit déclarée terminée lors d'un sprint de développement, elle doit satisfaire l'ensemble des critères suivants :
- **Code & Architecture :** Le code respecte les standards PSR-12, applique le patron 2 couches (Contrôleur mince -> Classe Service) et ne contient aucune duplication manifeste.
- **Sécurité :** Les entrées sont validées par des Form Requests, les failles CSRF/XSS sont neutralisées et les autorisations sont vérifiées via des Policies.
- **Tests Automatisés :** Les tests unitaires et d'intégration fonctionnels associés sont rédigés et passent avec succès (au vert).
- **Interface & Responsive :** L'affichage s'adapte sans rupture visuelle sur terminaux mobiles, tablettes et ordinateurs de bureau via Tailwind CSS et Preline UI.
- **Critères d'Acceptation :** L'ensemble des critères d'acceptation opérationnels définis dans la fiche de l'US sont testés et validés.
- **Revue & Documentation :** Le travail a fait l'objet d'une démonstration validée par le Product Owner lors de la Sprint Review.
