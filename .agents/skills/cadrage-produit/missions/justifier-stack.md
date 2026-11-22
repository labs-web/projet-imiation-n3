# Mission : Justification Rationnelle de la Stack Technique (`justifier-stack.md`)

## 1. Contexte & Rôle
Cette mission produit le **Dossier de justification technique de la stack** (`docs/cadrage/stack-technique.md`). Elle formalise pour tout projet web applicatif une analyse rationnelle et argumentée des choix technologiques de référence, démontrant leur pertinence au regard des besoins et des contraintes du produit.

---

## 2. Procédure Pas-à-Pas

1. **Identification des Exigences Métier et Techniques :**
   - Recueillir les besoins du projet : rapidité de livraison, volumétrie, réactivité d'interface, sécurité et maintenabilité.
   - Poser les critères de sélection : pérennité de l'écosystème, documentation disponible, robustesse et vélocité de développement.

2. **Analyse et Justification Composant par Composant :**
   Pour chaque brique de la solution de référence (ex: Laravel, MySQL, Tailwind, Preline UI, Alpine.js, Spatie) :
   - **Rôle du composant :** Définir la responsabilité précise de la brique au sein de l'architecture.
   - **Arguments de choix rationnels :** Exposer les atouts intrinsèques (ex: sécurité native, gain de temps, clarté architecturale, conformité aux standards).
   - **Bénéfices directs pour le projet :** Démontrer en quoi ce choix résout une contrainte concrète du produit par rapport aux alternatives.

3. **Composants Types de Référence d'un Projet Web Moderne :**
   - **Framework Backend :** Justifier le choix du framework (ex: Laravel 13) pour son écosystème modulaire, son ORM expressif et son outillage de tests.
   - **Système de Base de Données :** Justifier le SGBD relationnel (ex: MySQL) pour la cohérence transactionnelle ACID et sa maturité.
   - **Design System & UI :** Justifier l'approche utility-first (ex: Tailwind CSS) et la bibliothèque de composants (ex: Preline UI) pour l'accélération du développement et l'accessibilité.
   - **Réactivité Frontend :** Justifier la bibliothèque légère (ex: Alpine.js) pour injecter de l'interactivité sans l'overhead d'une SPA complète.
   - **Sécurité & Contrôle d'Accès :** Justifier la gestion déclarative des rôles et permissions (ex: Spatie Permission / Policies).

4. **Synthèse Coûts / Risques / Maintenabilité :**
   - Valider la cohérence globale de l'assemblage technique et l'absence de redondance.

5. **Rédaction du Livrable :**
   - Rédiger le document `docs/cadrage/stack-technique.md` au format Markdown pur sans aucun tableau.
