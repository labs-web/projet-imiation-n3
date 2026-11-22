# Mission : Planification et Cadrage d'un Jalon de Sprint (`planifier-jalon.md`)

## 1. Contexte & Rôle
Cette mission intervient au démarrage ou à la transition d'un jalon lors de l'exécution d'un sprint sur tout projet web. Elle consulte la feuille de route du sprint et découpe le travail en **jalons d'ingénierie maîtrisables** (2 à 4 étapes cohérentes par jalon).

---

## 2. Principes de Découpage des Jalons
Un jalon regroupe un ensemble cohérent d'étapes aboutissant à un incrément tangible :
- **Jalon de Cadrage & Socle :** Cadrage du projet, convention d'équipe, infrastructure Git et justification de stack.
- **Jalon de Conception & Définition :** Vision produit, personas usagers, Product Backlog initial et parcours utilisateurs.
- **Jalon de Prototypage & Maquettes :** UI Kit, maquettes d'écrans clés et validation des parcours.
- **Jalon d'Incrément Applicatif :** Réalisation de tranches verticales de code, tests automatisés et persistance.
- **Jalon de Clôture & Revue :** Démonstration de l'incrément, Sprint Review et Rétrospective.

---

## 3. Procédure Pas-à-Pas

1. **Identification du Jalon Courant :**
   - Vérifier les livrables déjà produits dans le workspace (`docs/`, `sprints/`, `scrum/`, `src/`).
   - Déterminer le jalon actif à exécuter selon la feuille de route du sprint.

2. **Élaboration du Plan de Jalon :**
   - Lister les étapes du jalon avec :
     - Les entrées requises (documents antérieurs, contexte ou références).
     - Les activités d'ingénierie précises à mener.
     - Les livrables exacts à produire (chemin canonique et critères de succès).
     - Les compétences ou outils mobilisés.

3. **Génération de l'Artéfact Interactif :**
   - Émettre un artéfact interactif standardisé (`plan-jalon-[id].md` avec `RequestFeedback: true`).
   - Présenter le plan au concepteur et suspendre toute modification en attente de son approbation (bouton *Proceed*).
