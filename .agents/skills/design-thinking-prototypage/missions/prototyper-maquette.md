# Mission : Prototypage de la Maquette Interactive en HTML & CSS (`prototyper-maquette.md`)

## 1. Contexte & Rôle
Cette mission produit la **Maquette interactive concrète en HTML et CSS** de l'application. Elle traduit le User Flow et l'UI Kit en un prototype visuel réel, directement visualisable et testable dans un navigateur web.

Le livrable comprend :
- Le fichier prototype autonome en HTML et CSS : `docs/conception/maquettes/index.html` (ou `docs/conception/maquette-accueil.html`), structuré avec Tailwind CSS, Preline UI et Alpine.js.
- La fiche de documentation d'ingénierie : `docs/conception/maquettes-sprint-1.md` décrivant l'architecture zonale, la grille responsive et liant le prototype.

---

## 2. Structure Normative du Prototype HTML & CSS

Le prototype HTML/CSS doit être un document autonome complet et exécutable :

1. **En-tête & Dépendances CSS/JS :**
   - Doctype HTML5 standard avec meta responsive (`viewport`).
   - Intégration de Tailwind CSS (via script CDN ou build compilé) et de la police de référence.
   - Intégration de la bibliothèque de composants Preline UI et du moteur réactif Alpine.js.

2. **Zones Fonctionnelles Composant la Maquette :**
   - **En-tête de Navigation (Navbar) :** Logo, liens d'accès, barre de recherche, bouton de connexion et menu hamburger responsive pour mobile.
   - **Hero Section :** Message d'accroche valorisant, sous-titre explicatif, statistiques clés et bouton d'action principal.
   - **Barre de Filtrage Interactive :** Sélecteur horizontal de catégories avec état actif mis en valeur et interactivité Alpine.js.
   - **Grille d'Articles Responsive :** Cartes d'articles soignées (1 colonne mobile, 2 colonnes tablette, 3 colonnes desktop) affichant titre, extrait, badge catégorie, nom de l'auteur et temps de lecture.
   - **Contrôles de Pagination :** Boutons de pagination accessibles (Précédent, numéros de page, Suivant).
   - **Pied de Page (Footer) :** Liens institutionnels, mentions légales et réseaux professionnels.

3. **Interactivité & Dynamisme Client :**
   - Utilisation des attributs Alpine.js (`x-data`, `x-show`, `x-on:click`) pour animer les menus, les filtres et les modales sans backend.

---

## 3. Structure Normative de la Documentation (`maquettes-sprint-1.md`)

Rédigée au format Markdown sans aucun tableau :
1. **Présentation de la Maquette :** Objectifs de test ergonomique et lien relatif direct vers le fichier HTML (`./maquettes/index.html`).
2. **Grille de Mise en Page & Responsive :** Comportement sur mobile (< 640px), tablette (640-1024px) et desktop (> 1024px).
3. **Inventaire Zonale des Écrans :** Détail des zones et composants mobilisés.
4. **Protocole de Test Utilisateur :** Instructions simples pour ouvrir et tester la maquette dans le navigateur.
