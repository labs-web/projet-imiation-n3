# Mission : Exécution Pas-à-Pas d'une Étape de Jalon (`executer-etape.md`)

## 1. Contexte & Rôle
Après validation du plan de jalon par le concepteur, cette mission prend en charge la réalisation effective des étapes, en s'assurant au préalable que la compétence requise est disponible.

---

## 2. Procédure Pas-à-Pas

1. **Vérification Préalable de Couverture en Compétence (Impératif) :**
   - Identifier l'étape du flux de travail à exécuter et son livrable.
   - Vérifier si un skill et une mission dédiés existent dans `.agents/skills/` pour cette étape (rappel : une mission peut couvrir plusieurs étapes).
   - **Si la compétence ou la mission est absente ou inadaptée :**
     - Suspendre immédiatement l'exécution directe.
     - Déclencher `/skills-planer` (mission `couvrir-etape-sprint.md`) pour arbitrer entre : la création d'un nouveau skill, l'ajout d'une mission dans un skill existant, ou une reconception.
     - Attendre la validation de l'artéfact interactif de compétence par le concepteur et la création physique du skill avant de reprendre l'étape.

2. **Vérification des Prérequis de l'Étape :**
   - S'assurer que les livrables des étapes antérieures sont disponibles et conformes.
   - Identifier l'emplacement cible du livrable (ex : `sprints/sprint-0.md`, `docs/cadrage/note-cadrage.md`).

3. **Réalisation de l'Activité d'Ingénierie via le Skill Dédié :**
   - Mobiliser le skill et la mission responsables de l'étape.
   - Produire le contenu technique en respectant scrupuleusement la stack de référence (Laravel 13, MySQL, Tailwind CSS avec Preline UI, Alpine.js).
   - Appliquer les règles de rédaction :
     - Français direct niveau A1/A2 (phrases courtes Sujet + Verbe + Complément).
     - Interdiction stricte de tout tableau Markdown (`| ... |`) : listes à puces directes (`- `) exclusives.
     - Liens relatifs exclusifs (`./`, `../`).

4. **Contrôle Qualité Immédiat :**
   - Vérifier la complétude et l'unicité du livrable généré.
   - Mettre à jour le document de suivi du sprint (`sprints/sprint-[N].md`) pour consigner l'avancement.

5. **Enchaînement ou Clôture :**
   - Répéter la procédure pour les étapes suivantes du jalon, ou basculer vers `missions/valider-jalon.md` une fois toutes les étapes du jalon terminées.
