# Feuille d'Engagement : Sprint 0

> Livrable d'ingénierie logicielle — Étape 10 du flux de développement (Cadre Scrum : Planification & Engagement d'Équipe).

---

## 1. Fiche d'Identification du Sprint 0

- **Intitulé du Sprint :** Sprint 0 — Cadrage, Immersion Usagers & Maquette de la Page d'Accueil.
- **Timebox :** 10 jours ouvrés (80 heures nominales indicatives).
- **Sprint Goal (Objectif d'Incrément) :**
  "Cadrer le périmètre initial du produit, formaliser la compréhension des usagers à travers les personas et le backlog MoSCoW, et livrer la maquette interactive responsive de la page d'accueil en HTML et CSS validée par le Product Owner lors de la Sprint Review 0."
- **Composition de l'Équipe Scrum :**
  - **Product Owner :** Groupe 1 (Porteur de la vision métier et des arbitrages fonctionnels).
  - **Scrum Master :** Groupe 3 (Facilitateur du cadre Scrum et garant des cérémonies agiles).
  - **Équipe de Développement :** Développeurs Full-Stack (responsables de la conception, des modèles et du prototypage HTML/CSS).
- **Capacité de l'Équipe :** 80 heures par développeur réparties sur les activités de cadrage, d'analyse et de maquettage.

---

## 2. Périmètre Sélectionné du Product Backlog (Sprint Backlog)

Pour atteindre le Sprint Goal, les User Stories prioritaires suivantes ont été sélectionnées depuis le Product Backlog initial ([scrum/product-backlog.md](../scrum/product-backlog.md)) :

- **US-01 (Must Have — 3 SP) :** Consultation de la liste des articles publiés sur la page d'accueil.
  - Objectif Sprint 0 : Prototyper la grille responsive de cartes d'articles et les informations d'en-tête.
- **US-02 (Must Have — 2 SP) :** Lecture d'un article complet.
  - Objectif Sprint 0 : Spécifier la hiérarchie typographique et la modale d'aperçu d'article.
- **US-03 (Must Have — 3 SP) :** Filtrage des articles par catégorie thématique.
  - Objectif Sprint 0 : Prototyper la barre de filtres interactive avec réactivité Alpine.js.
- **US-08 (Must Have — 3 SP) :** Administration du référentiel des catégories.
  - Objectif Sprint 0 : Intégrer les catégories types (Carrière, Laravel, Insertion, Architecture) dans l'UI Kit.
- **Total de l'Engagement :** 11 Story Points prototypés et validés lors de la maquette d'accueil.

---

## 3. Découpage en Tâches Techniques d'Ingénierie

Chaque exigence est décomposée en tâches techniques d'une charge maximale de 8 heures :

- **Tâche T-01 (6h) :** Cadrage du projet et formalisation de la note de cadrage avec objectifs SMART et matrice In-Scope vs Out-of-Scope (`docs/cadrage/note-cadrage.md`) — **Terminé**.
- **Tâche T-02 (4h) :** Justification rationnelle de la stack technique de référence Laravel 13, MySQL, Preline UI, Alpine.js (`docs/cadrage/stack-technique.md`) — **Terminé**.
- **Tâche T-03 (4h) :** Définition de la Vision Produit et du Product Goal fondateur (`docs/produit/vision-produit.md`) — **Terminé**.
- **Tâche T-04 (6h) :** Conduite de l'immersion terrain et formalisation de la Carte d'Empathie à 4 quadrants (`docs/analyse/empathie.md`) — **Terminé**.
- **Tâche T-05 (6h) :** Modélisation des 3 fiches Personas archétypales du Blog (`docs/analyse/personas.md`) — **Terminé**.
- **Tâche T-06 (6h) :** Conception, découpage INVEST et ordonnancement MoSCoW du Product Backlog initial (`scrum/product-backlog.md`) — **Terminé**.
- **Tâche T-07 (6h) :** Modélisation arborescente du User Flow textuel complet de la page d'accueil (`docs/conception/user-flow.md`) — **En cours**.
- **Tâche T-08 (6h) :** Spécification des design tokens et de l'UI Kit de composants Tailwind CSS et Preline UI (`docs/conception/ui-kit.md`) — **En cours**.
- **Tâche T-09 (8h) :** Prototypage et assemblage de la maquette interactive concrète en HTML et CSS de la page d'accueil (`docs/conception/maquettes/index.html` et `docs/conception/maquettes-sprint-1.md`) — **En cours**.
- **Tâche T-10 (4h) :** Préparation de la soutenance contradictoire de Sprint Review 0 (Jalon Go/No-Go) et animation de la Rétrospective d'équipe (`sprints/pv-review-0.md`, `sprints/retrospective-0.md`) — **À venir**.

---

## 4. Definition of Done (DoD) Spécifique au Sprint 0

Pour que l'incrément Maquette soit validé lors de la Sprint Review 0, les conditions suivantes doivent être rigoureusement satisfaites :
- **Prototype HTML/CSS autonome :** La maquette est codée en HTML5 valide et stylisée avec Tailwind CSS et Preline UI, directement visualisable dans tout navigateur web.
- **Adaptabilité Responsive :** La mise en page est testée et fluide sur formats mobile (< 640px), tablette (640-1024px) et écran large (> 1024px).
- **Interactivité Client :** Les composants interactifs (menu hamburger mobile, filtrage par catégorie, modale d'aperçu) fonctionnent sans erreur dans la console JavaScript.
- **Accessibilité :** Les contrastes de couleur respectent la norme WCAG niveau AA (ratio supérieur à 4.5:1).
- **Alignement Documentaire :** Le User Flow et l'UI Kit reflètent exactement l'état du prototype produit.
- **Validation Produit :** Démonstration effectuée devant le Product Owner et décision Go/No-Go formelle consignée.

---

## 5. Registre des Risques & Actions de Mitigation

- **Risque 1 : Dérive du périmètre vers le code applicatif backend (Scope Creep).**
  - *Impact :* Élevé.
  - *Action préventive :* Interdiction d'implémenter du code contrôleur ou de persistance MySQL lors du Sprint 0 ; focalisation exclusive sur la maquette visuelle HTML/CSS statique et dynamique côté client via Alpine.js.
- **Risque 2 : Rupture ergonomique sur terminaux mobiles.**
  - *Impact :* Moyen.
  - *Action préventive :* Application stricte de la démarche mobile-first dès la conception de la maquette.
