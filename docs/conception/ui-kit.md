# UI Kit & Design System : Blog des Lauréats

> Livrable d'ingénierie logicielle — Étape 13 du flux de développement (Design Thinking : Spécification du Design System).

---

## 1. Fondations Graphiques & Design Tokens (Tailwind CSS)

Le Design System du **Blog des Lauréats** est construit sur les standards officiels de **Tailwind CSS** et de la bibliothèque de composants accessibles **Preline UI**. Il assure une identité visuelle moderne, sobre et cohérente.

### A. Palette Chromatique
- **Couleur Primaire (Identité & Actions) :**
  - `indigo-600` (`#4f46e5`) : Couleur d'accentuation majeure, boutons d'action prioritaires, liens actifs et badges sélectionnés.
  - `indigo-700` (`#4338ca`) : État de survol (hover) des boutons primaires.
  - `indigo-50` (`#eef2ff`) : Arrière-plan doux des badges primaires et conteneurs actifs.
- **Couleurs Secondaires & Catégories :**
  - *Carrière & Insertion :* Émeraude (`emerald-600`, fond `emerald-50`, texte `emerald-700`).
  - *Technique & Laravel :* Ambre (`amber-600`, fond `amber-50`, texte `amber-700`).
  - *Architecture & Méthodologie :* Ciel (`sky-600`, fond `sky-50`, texte `sky-700`).
  - *Veille & Outils :* Violet (`purple-600`, fond `purple-50`, texte `purple-700`).
- **Neutres (Surfaces & Typographie) :**
  - Fond de page principal : `slate-50` (`#f8fafc`).
  - Fond des cartes et conteneurs : `white` (`#ffffff`).
  - Bordures subtiles : `slate-200` (`#e2e8f0`).
  - Titres et textes dominants : `slate-900` (`#0f172a`).
  - Textes secondaires et descriptions : `slate-600` (`#475569`).
  - Métadonnées et textes discrets : `slate-400` (`#94a3b8`).

### B. Échelle Typographique
- **Famille de police :** Police sans-serif moderne système / Inter (`font-sans`).
- **Niveaux de taille :**
  - `text-4xl` (36px, `font-extrabold`) : Titre principal de la Hero Section.
  - `text-2xl` (24px, `font-bold`) : Titres de sections majeures (ex: "Derniers articles publiés").
  - `text-xl` (20px, `font-semibold`) : Titres des cartes d'articles.
  - `text-base` (16px, `font-normal`) : Corps de texte et paragraphes descriptifs.
  - `text-sm` (14px, `font-medium`) : Éléments de navigation, boutons et formulaires.
  - `text-xs` (12px, `font-semibold`) : Badges de catégories et métadonnées d'auteurs.

### C. Rayons de Courbure & Ombres
- **Rayons de courbure :**
  - `rounded-lg` (8px) : Boutons d'action, champs de formulaire, badges.
  - `rounded-xl` (12px) : Cartes d'articles, bannières et conteneurs.
  - `rounded-full` : Avatars d'auteurs et puces de notification.
- **Élévations & Ombres :**
  - `shadow-sm` : Ombres douces pour les cartes au repos.
  - `shadow-md` / `shadow-lg` : Élévation dynamique au survol des cartes (`hover:shadow-md transition`).

---

## 2. Spécification des Composants d'Interface Réutilisables

### A. Boutons d'Action (Buttons)
- **Bouton Primaire :**
  - Classes Tailwind : `inline-flex items-center justify-center px-5 py-2.5 bg-indigo-600 text-white text-sm font-semibold rounded-lg hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 transition shadow-sm`.
  - Usage : Action principale (ex: "Explorer les articles", "Publier").
- **Bouton Secondaire / Outline :**
  - Classes Tailwind : `inline-flex items-center justify-center px-4 py-2 border border-slate-300 bg-white text-slate-700 text-sm font-medium rounded-lg hover:bg-slate-50 focus:outline-none focus:ring-2 focus:ring-slate-400 transition`.
  - Usage : Action d'annulation, filtres inactifs ou action d'appui.
- **Bouton Discret (Ghost) :**
  - Classes Tailwind : `inline-flex items-center px-3 py-1.5 text-sm font-medium text-slate-600 hover:text-indigo-600 hover:bg-slate-100 rounded-lg transition`.
  - Usage : Liens de navigation secondaire, actions de retour.

### B. Badges de Catégorie (Pills / Badges)
- **Badge Actif :** `px-3 py-1.5 text-xs font-semibold rounded-full bg-indigo-600 text-white shadow-sm`.
- **Badge Inactif (Filtre) :** `px-3 py-1.5 text-xs font-medium rounded-full bg-slate-100 text-slate-600 hover:bg-slate-200 cursor-pointer transition`.
- **Badge Catégorie d'Article :** `inline-flex items-center px-2.5 py-0.5 text-xs font-semibold rounded-full bg-emerald-50 text-emerald-700 border border-emerald-200`.

### C. Champ de Recherche (Search Input)
- **Classes Tailwind :** `block w-full pl-10 pr-4 py-2 text-sm bg-slate-50 border border-slate-200 rounded-lg text-slate-900 placeholder-slate-400 focus:bg-white focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:border-transparent transition`.
- **Accessoire visuel :** Icône loupe positionnée en absolu à gauche (`absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-slate-400`).

### D. Carte d'Article (Article Card Component)
- **Structure du composant :**
  - Conteneur : `flex flex-col bg-white border border-slate-200 rounded-xl overflow-hidden shadow-sm hover:shadow-md hover:-translate-y-0.5 transition duration-200`.
  - Image de couverture : `w-full h-48 object-cover bg-slate-100`.
  - Corps de carte (`p-5 flex-1 flex flex-col`) :
    - En-tête : Badge catégorie + temps de lecture (`text-xs text-slate-400`).
    - Titre : `text-lg font-bold text-slate-900 hover:text-indigo-600 line-clamp-2 transition mt-2`.
    - Extrait : `text-sm text-slate-600 line-clamp-3 mt-2 flex-1`.
  - Pied de carte (`pt-4 mt-4 border-t border-slate-100 flex items-center justify-between`) :
    - Auteur : Avatar circulaire (`w-8 h-8 rounded-full`), nom (`text-xs font-semibold text-slate-900`) et statut (`text-xs text-slate-500`).
    - Date : `text-xs text-slate-400`.

---

## 3. Composants de Mise en Page & Navigation

### A. Barre de Navigation (Navbar Preline UI)
- Fond blanc avec bordure inférieure `border-b border-slate-200 sticky top-0 z-50 backdrop-blur-md bg-white/95`.
- Disposition en conteneur centré `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`.
- Alignement flexible : Logo de gauche, liens de navigation centrale, espace utilisateur à droite.
- Bouton déclencheur mobile (Hamburger) avec transition fluide.

### B. Pied de Page (Footer Institutionnel)
- Fond `bg-slate-900 text-slate-300 py-12 border-t border-slate-800`.
- 3 colonnes d'information : Présentation du Blog des Lauréats, Liens rapides et Mentions écosystème Solicode Tanger.
- Zone de copyright inférieure avec mention des règles de gouvernance agile.

---

## 4. Règles d'Accessibilité (WCAG AA)

- **Contraste minimal :** Tous les textes normaux présentent un ratio de contraste supérieur à 4.5:1 face à leur arrière-plan.
- **Indicateurs de focus :** Chaque élément interactif (lien, bouton, champ) dispose d'un contour de focus visible (`focus:ring-2 focus:ring-indigo-500`).
- **Support des lecteurs d'écran :** Les boutons avec icône seule intègrent une étiquette textuelle masquée `aria-label` ou `sr-only`.
