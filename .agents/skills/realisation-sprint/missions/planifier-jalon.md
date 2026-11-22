# Mission : Planification et Cadrage d'un Jalon de Sprint (`planifier-jalon.md`)

## 1. Contexte & Rôle
Cette mission intervient au démarrage ou à la transition d'un jalon lors de l'exécution d'un sprint. Elle consulte le document opérationnel de la session (`flux-travail/sessions/flux-travail-s{N}.md`) et structure le travail à venir en un **jalon d'ingénierie maîtrisable** (2 à 4 étapes cohérentes).

---

## 2. Découpage Type des Jalons (Exemple Session S0)
Pour le Sprint 0 (`flux-travail-s0.md`), les étapes d'application projet (UA.351.01 et UA.351.02) sont regroupées en 3 jalons :
- **Jalon 1 : Cadrage, Gouvernance & Infrastructure Git** (Étapes 11 à 14 : `sprint-0.md`, `README.md`, `note-cadrage.md`, `stack-technique.md`).
- **Jalon 2 : Vision Produit, Personas & Backlog Initial** (Étapes 15 et 16 : `vision-produit.md`, `personas.md`, `product-backlog.md`).
- **Jalon 3 : Incrément Maquette de la Page d'Accueil & Clôture Sprint 0** (Étapes 17 et 18 : `ui-kit.md`, `maquettes-sprint-1.md`, `pv-review-0.md`, `retrospective-0.md`).

---

## 3. Procédure Pas-à-Pas

1. **Identification du Jalon Courant :**
   - Vérifier les livrables déjà produits dans le workspace (`docs/`, `sprints/`, `scrum/`, `src/`).
   - Déterminer le jalon actif à exécuter.

2. **Élaboration du Plan de Jalon :**
   - Lister les étapes du jalon avec :
     - Les entrées requises (documents antérieurs ou références).
     - Les activités d'ingénierie précises à mener.
     - Les livrables exacts à produire (chemin canonique et critères de succès).
     - Les compétences ou outils mobilisés.

3. **Génération de l'Artéfact Interactif :**
   - Émettre un artéfact interactif standardisé (`plan-jalon-[N]-[id].md` avec `RequestFeedback: true`).
   - Présenter le plan au concepteur et suspendre toute modification en attente de son approbation (bouton *Proceed*).
