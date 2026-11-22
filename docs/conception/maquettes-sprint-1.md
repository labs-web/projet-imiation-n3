# Spécification de la Maquette d'Accueil : Blog des Lauréats

> Livrable d'ingénierie logicielle — Étape 13 du flux de développement (Design Thinking : Spécification & Prototype de la Maquette).

---

## 1. Prototype Concret en HTML et CSS

Conformément aux directives d'ingénierie, la maquette interactive de la page d'accueil a été entièrement codée en **HTML5 et CSS** sous forme de prototype autonome exécutable dans n'importe quel navigateur web.

- **Accès direct au prototype interactif :**
  👉 [Consulter la Maquette HTML & CSS (docs/conception/maquettes/index.html)](./maquettes/index.html)
- **Stack de la Maquette :**
  - Balisage : HTML5 sémantique.
  - Styles : Classes officielles Tailwind CSS.
  - Composants : Bibliothèque de composants accessibles Preline UI.
  - Dynamisme client : Alpine.js pour le filtrage en temps réel, le menu mobile et la modale de lecture.

---

## 2. Découpage Structurel & Architecture Zonale de l'Écran

La page d'accueil est découpée en 6 zones fonctionnelles coordonnées :

### Zone 1 : En-tête de Navigation (Navbar Preline UI)
- **Position :** Fixe en haut de l'écran (`sticky top-0 z-40`) avec fond semi-transparent flouté (`backdrop-blur-md`).
- **Contenu :**
  - Logo distinctif "BL" et intitulé "Blog des Lauréats — Solicode Tanger".
  - Liens de navigation directe (Accueil, Articles, À propos, Lauréats).
  - Champ de recherche en temps réel intégré avec icône loupe.
  - Bouton d'accès rapide "Espace Lauréat" pour les contributeurs.
  - Déclencheur de menu hamburger pour les écrans mobiles (< 768px).

### Zone 2 : Hero Section & Proposition de Valeur
- **Objectif :** Capter l'attention du visiteur et clarifier la proposition de valeur en moins de 3 secondes.
- **Contenu :**
  - Badge pulsant d'identification de la communauté.
  - Titre d'accroche valorisant l'expérience terrain des anciens.
  - Paragraphe d'orientation pour les apprenants et recruteurs.
  - Double bouton d'action (Call-to-Action) : "Explorer les articles" et "Découvrir la démarche".
  - Grille d'indicateurs d'impact : 30+ Lauréats, 50+ Articles, 100% Retours réels, Temps de réponse $< 300$ ms.

### Zone 3 : Barre de Filtrage par Catégorie (Alpine.js)
- **Objectif :** Permettre un filtrage immédiat et sans rechargement lourd des articles selon les thématiques du backlog.
- **Boutons de filtres interactifs :**
  - *Tous* (sélectionné par défaut avec compteur dynamique).
  - *Conseils Carrière* (badge vert émeraude).
  - *Tutoriels Laravel* (badge ambre).
  - *Insertion Professionnelle* (badge indigo).
  - *Architecture & Bonnes Pratiques* (badge ciel).
- **Comportement :** Le clic sur un filtre met à jour la variable réactive `activeCategory` et masque instantanément les articles non concernés.

### Zone 4 : Grille d'Articles Responsive
- **Disposition :**
  - Mobile (< 640px) : 1 colonne verticale optimisée pour la navigation tactile.
  - Tablette (640px à 1024px) : Grille à 2 colonnes équilibrées.
  - Desktop (> 1024px) : Grille à 3 colonnes soignées avec espacement régulier (`gap-6`).
- **Composant Carte d'Article :**
  - Badge de catégorie avec code couleur sémantique.
  - Temps de lecture estimé automatique (ex: "6 min de lecture").
  - Titre accrocheur et extrait narratif tronqué à 3 lignes.
  - Fiche auteur avec avatar circulaire, nom complet, date de parution et flèche de lecture.
  - Effet dynamique d'élévation au survol (`hover:-translate-y-1 hover:shadow-md`).

### Zone 5 : Modale Interactive de Lecture Rapide
- **Objectif :** Offrir une expérience de consultation fluide sans quitter la page d'accueil.
- **Déclenchement :** Clic sur n'importe quelle carte d'article.
- **Contenu :** Titre complet, statut et biographie de l'auteur lauréat, corps de texte structuré et bouton de fermeture.

### Zone 6 : Pied de Page (Footer)
- **Disposition :** Fond sombre `slate-900` avec 3 colonnes de contenu (Présentation, Thématiques clés, Cadre institutionnel et encadrement).
- **Mentions :** Copyright 2026 et rappel des normes de réalisation agile.

---

## 3. Grille Responsive & Breakpoints

- **Mobile (< 640px) :**
  - Grille d'articles à 1 colonne.
  - Menu de navigation replié sous bouton hamburger.
  - Filtres horizontaux défilables au doigt.
  - Statistiques en grille 2x2 compacte.
- **Tablette (640px à 1024px) :**
  - Grille d'articles à 2 colonnes.
  - Barre de recherche condensée.
- **Desktop (> 1024px) :**
  - Grille d'articles à 3 colonnes.
  - Navigation complète déployée avec champ de recherche élargi.

---

## 4. Protocole de Test Utilisateur pour la Sprint Review 0

Pour la démonstration contradictoire lors de la Sprint Review 0, le protocole suivant est appliqué sur le fichier [maquettes/index.html](./maquettes/index.html) :

1. **Test 1 — Navigation et Découverte :**
   - Ouvrir `docs/conception/maquettes/index.html` dans Chrome ou Edge.
   - Constater l'affichage immédiat de la Hero Section et des statistiques clés.
2. **Test 2 — Filtrage Réactif :**
   - Cliquer successivement sur "Conseils Carrière", "Tutoriels Laravel" et "Tous".
   - Vérifier que la grille se met à jour instantanément sans scintillement ni rechargement.
3. **Test 3 — Recherche Textuelle :**
   - Taper "test technique" ou "Service" dans le champ de recherche.
   - Vérifier le filtrage instantané des cartes correspondantes.
4. **Test 4 — Lecture Rapide (Modale) :**
   - Cliquer sur la première carte pour afficher la modale complète.
   - Vérifier la fluidité de fermeture par le bouton "Fermer" ou clic à l'extérieur.
5. **Test 5 — Responsive Design :**
   - Réduire la largeur de la fenêtre à 375px (format smartphone).
   - Constater le passage en 1 colonne et tester l'ouverture du menu hamburger.
