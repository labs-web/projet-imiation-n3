# Mission : Génération de l'Artéfact Interactif de Révision (`generer-artefact-revision.md`)

## 1. Objectif
Rédiger un artéfact interactif standardisé (`plan-revision-[cible].md`) permettant au concepteur de relire, commenter et valider (via le bouton *Proceed*) l'ensemble des ajustements ligne par ligne ainsi que la matrice des skills à adapter.

---

## 2. Structure Obligatoire de l'Artéfact

L'artéfact interactif doit comporter obligatoirement :
- **Métadonnées de l'artéfact :**
  - `UserFacing: true`
  - `RequestFeedback: true`
  - `Summary`: Résumé clair des modifications proposées et des skills impactés.
- **Section 1 : User Review Required (Alertes Clés)** :
  - Mettre en évidence les décisions d'architecture ou les changements pédagogiques majeurs.
- **Section 2 : Cartographie Ligne par Ligne des Modifications** :
  - Présenter chaque section cible avec les numéros de lignes précis.
  - Exposer l'état actuel du document.
  - Détailler la modification proposée et la règle ou consigne qui la justifie.
- **Section 3 : Matrice des Skills Impactés** :
  - Pour chaque skill concerné, préciser le fichier cible (`SKILL.md` ou `missions/<mission>.md`) et la nature de la mise à jour à apporter.
- **Section 4 : Plan d'Exécution et Vérification** :
  - Découpage séquentiel des opérations de modification et tests automatisés.

---

## 3. Règles de Formatage
- **Zéro tableau Markdown (`| ... |` interdit) :** Structurer exclusivement sous forme de listes à puces directes (`- `).
- **Zéro code numérique `UA.*` :** Désignations descriptives et sémantiques.
- Liens relatifs vers les fichiers modifiés.
