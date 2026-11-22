# Mission : Prototypage de la Maquette Interactive (`prototyper-maquette.md`)

## 1. Contexte & Rôle
Cette mission produit les **Maquettes interactives et responsives** de l'application formalisées dans `docs/conception/maquettes-sprint-1.md`. Elle traduit le User Flow et l'UI Kit en un prototype concret et testable de l'écran principal.

---

## 2. Structure Normative du Document de Maquette

Le document est rédigé sans tableau Markdown :

1. **Architecture Visuelle & Grille de Mise en Page :**
   - Découpage en zones structurelles (Header, Hero, Filtres, Grille de contenu, Footer).
   - Déclinaison responsive : comportement sur mobile (< 640px), tablette (640-1024px) et desktop (> 1024px).

2. **Description Détaillée Zone par Zone :**
   - **Zone 1 — En-tête de Navigation (Navbar) :** Logo, liens d'accès direct, barre de recherche, bouton de connexion.
   - **Zone 2 — Hero Section :** Titre d'accroche valorisant, sous-titre explicatif, appel à l'action principal.
   - **Zone 3 — Barre de Filtrage par Catégorie :** Sélecteur horizontal de filtres avec état actif mis en valeur.
   - **Zone 4 — Grille d'Articles :** Disposition en cartes responsives (1 colonne mobile, 2 colonnes tablette, 3 colonnes desktop) affichant titre, extrait, auteur, date et badge catégorie.
   - **Zone 5 — Pagination :** Contrôles de navigation entre les pages de résultats.
   - **Zone 6 — Pied de Page (Footer) :** Informations de contact, liens institutionnels et crédits.

3. **Prototype de Balisage Concret (Balisage Tailwind CSS + Preline UI) :**
   - Code Blade/HTML d'intégration prêt à l'emploi utilisant les classes officielles de Tailwind CSS et la bibliothèque Preline UI.
   - Démonstration des interactions avec attributs déclaratifs Alpine.js (menus déroulants, filtres réactifs).

4. **Spécification des Interactions & Transitions :**
   - Effets de survol, micro-animations et comportement en cas d'écran étroit (menu hamburger mobile).
