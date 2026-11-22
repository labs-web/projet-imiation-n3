# Procès-Verbal de Sprint Review 0 (Jalon Go / No-Go)

> Livrable d'ingénierie logicielle — Étape 10 du flux générique (Cadre Scrum : Revue de Sprint & Jalon Go/No-Go).

---

## 1. Fiche d'Identification de la Séance

- **Sprint évalué :** Sprint 0 — Cadrage, Immersion Usagers & Maquette de la Page d'Accueil.
- **Date de la séance :** 22 Novembre 2026.
- **Lieu & Modalité :** Salle de revue agile / Session contradictoire de validation.
- **Participants :**
  - **Product Owner :** Groupe 1 (Validation de la conformité métier et des attentes usagers).
  - **Scrum Master :** Groupe 3 (Facilitation de la séance et vérification du respect de la DoD).
  - **Équipe de Développement :** Développeurs Full-Stack (Présentation technique et démonstration de la maquette).
  - **Encadrant Référent :** ESSARRAJ Fouad (Supervision de la démarche d'ingénierie).
- **Rappel du Sprint Goal :**
  "Cadrer le périmètre initial du produit, formaliser la compréhension des usagers à travers les personas et le backlog MoSCoW, et livrer la maquette interactive responsive de la page d'accueil en HTML et CSS validée par le Product Owner lors de la Sprint Review 0."

---

## 2. Démonstration Contradictoire de l'Incrément Maquette

La démonstration s'est appuyée directement sur le prototype réel en HTML et CSS [docs/conception/maquettes/index.html](../docs/conception/maquettes/index.html) ouvert dans le navigateur web.

### Scénarios Déroulés en Séance :
1. **Atterrissage & Découverte de la Hero Section :**
   - Constat du chargement instantané de la page d'accueil.
   - Vérification de la clarté du message d'accroche et des 4 indicateurs d'impact (30+ Lauréats, 50+ Articles, 100% Retours réels, $< 300$ ms).
2. **Filtrage Dynamique par Catégorie (Alpine.js) :**
   - Clic successif sur les badges "Conseils Carrière", "Tutoriels Laravel", "Insertion" et "Architecture".
   - Constat de la mise à jour instantanée de la grille sans rechargement de page.
   - Test de réinitialisation avec le badge "Tous".
3. **Recherche Textuelle en Direct :**
   - Saisie des termes "test technique" et "Service".
   - Filtrage instantané des cartes d'articles correspondantes.
4. **Lecture Rapide en Modale Interactive :**
   - Clic sur la carte d'article de Sara Benjelloun.
   - Affichage fluide de la modale avec biographie de l'auteure, extrait narratif et corps de texte structuré.
   - Fermeture par bouton ou clic extérieur.
5. **Comportement Responsive & Accessibilité :**
   - Redimensionnement de la fenêtre en format mobile (375px).
   - Constat du basculement en colonne unique et vérification de l'ouverture du menu tiroir hamburger.

### Verbatims et Retours du Product Owner :
- *"Le choix d'avoir produit une maquette concrète en HTML et CSS plutôt qu'une simple description textuelle permet de valider directement l'expérience utilisateur réelle."*
- *"La navigation est très fluide, les filtres par catégorie fonctionnent parfaitement et la modale de lecture est une excellente surprise pour la consultation rapide."*
- *"L'UI Kit est sobre, moderne et parfaitement aligné avec l'identité de l'établissement."*

---

## 3. Audit de Conformité à la Definition of Done (DoD)

Chaque critère de la Definition of Done définie dans `sprints/sprint-0.md` a été rigoureusement audité :

- **Prototype autonome en HTML et CSS :** Conforme (fichier `docs/conception/maquettes/index.html` exécutable dans tout navigateur).
- **Adaptabilité Responsive :** Conforme (testé et validé sur mobile 375px, tablette 768px et desktop 1280px).
- **Interactivité Client (Alpine.js) :** Conforme (zéro erreur dans la console JavaScript du navigateur).
- **Accessibilité des Contrastes (WCAG AA) :** Conforme (ratios de contraste supérieurs à 4.5:1 sur l'ensemble des textes et badges).
- **Synchronisation du User Flow et de l'UI Kit :** Conforme (`user-flow.md` et `ui-kit.md` reflètent fidèlement la maquette).
- **Validation Formelle du Product Owner :** Conforme (approbation sans réserve lors de la démonstration).

---

## 4. Bilan d'Acceptation des User Stories (Sprint Backlog)

- **US-01 : Consultation de la liste des articles publiés (3 SP)**
  - Statut : **Acceptée** (grille d'articles 100% conforme et responsive).
- **US-02 : Lecture d'un article complet (2 SP)**
  - Statut : **Acceptée** (typographie lisible et modale de lecture rapide fonctionnelle).
- **US-03 : Filtrage des articles par catégorie (3 SP)**
  - Statut : **Acceptée** (filtres interactifs Alpine.js sans rechargement).
- **US-08 : Gestion du référentiel des catégories (3 SP)**
  - Statut : **Acceptée** (catégories intégrées de façon cohérente dans l'UI Kit et les filtres).
- **Bilan de Vélocité :** 11 Story Points engagés, 11 Story Points validés (Taux de complétude : 100%).

---

## 5. Décision Collégiale du Jalon : Arbitrage Go / No-Go

À l'issue de la démonstration et de l'audit DoD, le Product Owner et l'équipe prononcent à l'unanimité :

> ### **DÉCISION DU JALON : GO !**
> **Autorisation officielle :** La phase de cadrage et de maquettage du Sprint 0 est déclarée achevée avec succès.
> Le lancement du **Sprint 1 (Delivery applicatif Laravel : Socle technique, architecture 2 couches MVC + Service et persistance MySQL)** est formellement autorisé.

### Recommandations pour le Sprint 1 :
- Conserver la même charte de composants Preline UI lors de la création des gabarits Blade Laravel.
- Structurer le code backend selon le patron contrôleur mince vers classe de service dès la première fonctionnalité.
