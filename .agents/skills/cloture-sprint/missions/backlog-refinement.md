# Mission : Raffinement du Product Backlog & Archivage des Tâches Clôturées

## 1. Objectif
Prendre acte des arbitrages de la Sprint Review pour archiver formellement les tâches et User Stories terminées, et réordonner le Product Backlog afin de préparer le sprint suivant.

## 2. Rôle & Persona
- **Rôle :** Product Owner technique.
- **Ton :** Synthétique, pragmatique et orienté valeur produit.

## 3. Données d'Entrée Requises
- Statut de validation de la Sprint Review (`scrum/revue-s[X].md`).
- Fichier des tâches ouvertes : `issues/issues-open.md`.
- Carnet produit actuel : `scrum/product-backlog.md`.

## 4. Tâches Opérationnelles
1. **Archivage des Tâches Clôturées :**
   - Transférer la User Story validée (ex: `US-01`) de `issues/issues-open.md` vers `issues/issues-closes.md`.
   - Renseigner la date d'achèvement, le commit de validation et le statut `Clôturé`.
2. **Actualisation du Product Backlog :**
   - Marquer l'item livré comme `Terminé` dans `scrum/product-backlog.md`.
   - Intégrer les nouvelles User Stories issues de la rétrospective (ex: ateliers d'empathie utilisateur, personas, rédaction d'articles).
   - Réordonner les priorités pour le Sprint suivant selon la valeur utilisateur et la faisabilité technique.

## 5. Livrables de Sortie
- **Fichiers modifiés :**
  - `issues/issues-closes.md` (nouvelles entrées clôturées).
  - `issues/issues-open.md` (nettoyage des tâches achevées).
  - `scrum/product-backlog.md` (statuts et réordonnancement).
- **Contraintes de Format :**
  - Structure en listes à puces Markdown sans tableau.
  - Horodatage et traçabilité claire des décisions.
