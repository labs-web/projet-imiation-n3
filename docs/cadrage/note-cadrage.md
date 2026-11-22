# Note de Cadrage du Projet : Blog des Lauréats

> Livrable d'ingénierie logicielle — Étape 2 du flux de développement (Cadrage & Périmètre Produit).

---

## 1. Contexte & Enjeux Stratégiques

### Contexte Général
Le projet répond au besoin de structurer et d'animer le réseau des lauréats et des apprenants.
Actuellement, les retours d'expérience et conseils de carrière sont dispersés sur des réseaux sociaux tiers ou partagés de manière informelle, sans capitalisation pérenne.

### Proposition de Valeur
Le **Blog des Lauréats** offre un média numérique institutionnel et convivial dédié :
- Permettre aux lauréats de documenter leurs réalisations, parcours et expertises professionnelles.
- Permettre aux apprenants en cours de formation d'accéder directement à des retours d'expérience concrets.
- Valoriser l'excellence technique et le dynamisme de la communauté.

---

## 2. Objectifs Stratégiques & SMART

Les objectifs de réalisation du produit sont formulés selon les critères SMART :

- **Spécifique (S) :** Concevoir, développer et déployer une plateforme web autonome permettant la rédaction, la relecture éditoriale, la publication et la consultation d'articles professionnels classés par catégories.
- **Mesurable (M) :**
  - Capacité d'accueil initiale : héberger au minimum 50 articles publiés lors du premier trimestre.
  - Temps d'accès : temps de chargement d'un article inférieur à 300 millisecondes en conditions normales.
  - Disponibilité et portabilité : interface 100% accessible et responsive sur terminaux mobiles, tablettes et ordinateurs de bureau.
- **Atteignable (A) :** Réalisation incrémentale structurée en sprints Scrum courts (itérations de 80 heures) avec livraison de tranches verticales de fonctionnalités testées de bout en bout.
- **Réaliste (R) :** Utilisation d'une stack technologique robuste et standardisée (Laravel 13, MySQL, Tailwind CSS, Preline UI, Alpine.js) évitant la surcomplexité technique et la dette architecturale.
- **Temporellement défini (T) :**
  - Sprint 0 : Finalisation du cadrage, de l'infrastructure et des prototypes validés.
  - Sprint 1 : Socle technique, persistance et première tranche fonctionnelle opérationnelle.
  - Clôture : Déploiement et mise en production à la fin du cycle agile.

---

## 3. Matrice de Périmètre (In-Scope vs Out-of-Scope)

Pour sécuriser la livraison dans les délais et garantir un niveau de qualité professionnel, le périmètre du Produit Minimum Viable (MVP) est délimité de façon stricte.

### In-Scope (Dans le périmètre officiel du MVP)
- **Consultation Publique :**
  - Affichage de la page d'accueil avec mise en avant des derniers articles parus.
  - Page de lecture détaillée d'un article avec typographie soignée et métadonnées (auteur, date, catégorie).
  - Filtrage des articles par catégories thématiques et moteur de recherche textuel simple.
  - Pagination dynamique des listes d'articles.
- **Espace Auteur (Lauréat) :**
  - Authentification sécurisée (inscription, connexion, réinitialisation de mot de passe).
  - Gestion du profil lauréat (nom, biographie, photo, liens professionnels LinkedIn et GitHub).
  - Tableau de bord personnel de suivi de ses articles.
  - Module de rédaction d'article avec éditeur riche épuré.
  - Cycle de vie de l'article : statut Brouillon, statut Soumis pour modération, statut Publié.
- **Espace d'Administration & Modération :**
  - Tableau de bord de supervision des articles soumis.
  - Actions de validation, publication ou demande de correction avec motif.
  - Gestion du référentiel des catégories (création, modification, archivage).
  - Gestion des utilisateurs et affectation des rôles RBAC.

### Out-of-Scope (Formellement exclu du MVP et différé)
- Messagerie instantanée ou chat en direct entre usagers (les contacts s'effectuent via les profils externes).
- Module d'abonnements payants, dons ou monétisation e-commerce.
- Application mobile native dédiée iOS / Android (l'expérience responsive mobile web couvre l'ensemble des besoins).
- Système complexe de notation étoilée ou algorithmes prédictifs de recommandation par IA.
- Importation / exportation automatisée d'articles depuis des plateformes externes (ex: Medium, WordPress).

---

## 4. Analyse des Contraintes et Facteurs Clés de Succès

### Contraintes Techniques
- Hébergement sur architecture serveur PHP / MySQL classique sans dépendance à des infrastructures propriétaires complexes.
- Respect strict du patron architectural en 2 couches (Contrôleur mince -> Classe Service métier).
- Zéro dépendance lourde de rendu côté client (SPA monolithique écartée au profit du rendu Blade enrichi par Alpine.js).

### Contraintes Réglementaires (RGPD)
- Consentement explicite lors de la création de compte.
- Droit d'accès, de rectification et de suppression des données personnelles pour chaque auteur.
- Protection stricte des données stockées (hachage des mots de passe, protection contre les failles courantes).

### Contraintes d'Accessibilité et d'Ergonomie
- Respect des règles de contraste visuel (normes WCAG niveau AA).
- Ergonomie mobile-first assurant une lisibilité exemplaire sur smartphones.
- Balisage HTML5 sémantique garantissant le bon fonctionnement des lecteurs d'écran.

### Facteurs Clés de Succès
- Simplicité et rapidité du parcours de rédaction pour les lauréats.
- Qualité et clarté de l'expérience de lecture pour les apprenants.
- Fluidité du processus de modération éditoriale.
