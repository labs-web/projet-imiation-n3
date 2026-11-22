# Mission : Conception de l'UI Kit Modulaire (`concevoir-ui-kit.md`)

## 1. Contexte & Rôle
Cette mission produit le document de spécification de l'**UI Kit officiel** formalisé dans `docs/conception/ui-kit.md`. Elle garantit la cohérence graphique, l'accessibilité et la réutilisabilité des composants visuels basés sur Tailwind CSS et Preline UI.

---

## 2. Structure Normative de l'UI Kit

Le document est rédigé sans tableau Markdown :

1. **Design Tokens & Fondations Graphiques :**
   - **Palette Chromatique :** Couleurs primaires, secondaires, neutres (gris) et sémantiques (succès, alerte, erreur), avec leurs codes de classes Tailwind (ex: `indigo-600`, `slate-900`).
   - **Échelle Typographique :** Polices de caractères, graisses et hiérarchie des tailles (`text-xs` à `text-4xl`).
   - **Espacements & Rayons de Courbure :** Règles de marge, padding et arrondis (`rounded-lg`, `rounded-xl`).
   - **Ombres & Élévations :** Styles d'élévation visuelle (`shadow-sm`, `shadow-md`).

2. **Composants d'Interface Réutilisables :**
   Pour chaque composant : description, classes Tailwind de référence, états (normal, survol, focus, désactivé) :
   - Boutons d'action (primaire, secondaire, discret/ghost).
   - Badges et tags de catégories.
   - Champs de formulaire et zones de recherche.
   - Cartes de contenu (Cards) avec image, en-tête, extrait et métadonnées.
   - Alertes et bannières de notification.

3. **Composants de Navigation & Mise en Page :**
   - Barre de navigation supérieure (Navbar) avec logo, liens et menu utilisateur.
   - Pied de page (Footer) avec liens de navigation et mentions légales.

4. **Critères d'Accessibilité (a11y) :**
   - Ratios de contraste vérifiés (norme WCAG niveau AA).
   - Indicateurs de focus visibles pour la navigation au clavier.
