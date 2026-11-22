# Bilan de Rétrospective Agile : Sprint 0

> Livrable d'ingénierie logicielle — Étape 11 du flux générique (Cadre Scrum : Amélioration Continue & Clôture de Sprint).

---

## 1. Fiche d'Identification de la Séance

- **Sprint évalué :** Sprint 0 — Cadrage, Immersion Usagers & Maquette de la Page d'Accueil.
- **Date de la séance :** 22 Novembre 2026.
- **Participants :** Équipe de réalisation Full-Stack, Scrum Master facilitateur.
- **Méthode d'animation :** Modèle des 4 Piliers d'Inspection (Forces, Freins, Enseignements, Actions).
- **Cadre de Travail :** Règle de sécurité psychologique de Norman Kerth :
  *"Quels que soient les constats établis, nous reconnaissons sincèrement que chacun a fait le meilleur travail possible compte tenu de ses compétences, de ses ressources et du contexte du moment."*

---

## 2. Bilan Réflexif Structuré (Les 4 Piliers d'Inspection)

### A. Ce qui a bien fonctionné (Forces & Réussites de l'Équipe)
- **Maquette concrète en HTML et CSS :** Avoir produit un prototype fonctionnel et autonome avec Tailwind CSS et Alpine.js a permis une démonstration vivante et immédiate devant le Product Owner, sans aucune ambiguïté d'interprétation.
- **Découpage granulaire en jalons :** La progression rythmée par jalons de 2 à 4 étapes (Cadrage -> Usagers -> Prototypage -> Revue) a éliminé le risque d'effet tunnel et sécurisé la qualité à chaque étape.
- **Immersion empathique incarnée :** La création des personas archétypaux (Youssef l'apprenant et Sara la lauréate) a servi de boussole permanente pour trancher rapidement les arbitrages de design.
- **Standardisation des compétences :** L'écosystème de compétences dans `.agents/skills/` (100% génériques, zéro tableau Markdown, $\le 75$ lignes) a assuré une cohérence documentaire remarquable.

### B. Ce qui a ralenti ou posé problème (Freins & Frustrations)
- **Spécificités projet initialement trop figées :** Les premières compétences créées contenaient des éléments en dur (noms de projet, mentions didactiques de tutoriels/labs), ce qui a exigé une phase de refonte générique pour respecter l'indépendance d'un vrai projet logiciel.
- **Vigilance continue sur les tableaux Markdown :** La tentation récurrente d'utiliser des tableaux avec barres verticales a nécessité une discipline stricte pour privilégier systématiquement les listes à puces directes.

### C. Ce qu'on a appris (Enseignements & Retours d'Expérience - REX)
- **Découplage strict Méthode vs Données :** Un skill professionnel doit porter la méthodologie d'ingénierie et la structure attendue, tandis que les données du projet doivent être injectées dynamiquement au moment de l'exécution.
- **Puissance d'Alpine.js pour le maquettage :** Alpine.js combiné aux classes utilitaires Tailwind permet de prototyper des interactions complexes (filtres instantanés, modales, menus déroulants) en quelques lignes sans recourir à un framework SPA lourd.
- **Valeur des User Stories INVEST :** Avoir des critères d'acceptation testables dès le début a rendu l'audit DoD lors de la Sprint Review immédiat et indiscutable.

---

## 3. Plan d'Actions d'Amélioration Continue (Sprint 1)

Pour aborder le premier sprint de delivery applicatif Laravel dans des conditions optimales, l'équipe s'engage sur 3 actions concrètes :

### Action 1 : Pureté de l'Architecture en 2 Couches (Contrôleur -> Service)
- **Engagement :** Isoler l'intégralité de la logique métier et des requêtes complexes dans des classes de service dédiées (`App\Services\ArticleService`) afin de maintenir les contrôleurs HTTP minces ($< 50$ lignes de code).
- **Responsable :** Équipe de Développement Full-Stack.
- **Indicateur de succès :** Zéro requête Eloquent complexe ou calcul métier directement logé dans les contrôleurs lors des revues de code.

### Action 2 : Approche Test-First (TDD Léger)
- **Engagement :** Rédiger systématiquement le test fonctionnel (Feature Test Laravel) avant ou conjointement à l'implémentation de chaque route pour sécuriser les régressions.
- **Responsable :** Référent Qualité & Tests.
- **Indicateur de succès :** 100% des tests de fonctionnalités passent au vert (`php artisan test`) lors de la démonstration du Sprint 1.

### Action 3 : Commits Atomiques Réguliers sous Souveraineté Humaine
- **Engagement :** Réaliser un commit Git explicite après chaque étape d'ingénierie validée en respectant la convention de nommage (`feat:`, `docs:`, `test:`, `refactor:`).
- **Responsable :** Scrum Master & Développeurs.
- **Indicateur de succès :** Un historique Git limpide reflétant l'avancement pas-à-pas sur la branche `sprint1`.

---

## 4. Clôture Formelle du Sprint 0

L'ensemble des objectifs du Sprint 0 ayant été accompli et validé :
- Le Sprint 0 est **officiellement clôturé**.
- L'équipe agile est autorisée à basculer sur la préparation et l'exécution du **Sprint 1 (Delivery applicatif Laravel)**.
