# Mission : Modélisation du User Flow Textuel (`modeliser-user-flow.md`)

## 1. Contexte & Rôle
Cette mission produit le document de **User Flow** formalisé dans `docs/conception/user-flow.md`. Elle décrit de façon textuelle, déclarative et arborescente les chemins empruntés par les utilisateurs pour accomplir leurs objectifs sur l'application.

---

## 2. Structure Normative du User Flow

Le document est rédigé sans tableau Markdown :

1. **Objectifs & Acteurs du Flux :**
   - Identification des Personas concernés par le parcours.
   - Déclencheurs initiaux et intention principale de l'utilisateur.

2. **Cartographie Arborescente Pas-à-Pas du Parcours :**
   Pour chaque étape du flux :
   - **Point d'entrée :** Écran ou composant d'atterrissage.
   - **Action utilisateur :** Geste ou décision concrète (clic, survol, saisie, défilement).
   - **Réaction du système :** Comportement visuel immédiat, chargement, transition.
   - **Conditions & Décisions :** Embranchements logiques (succès, absence de résultat, droits d'accès).
   - **Écran d'arrivée :** État final ou étape suivante.

3. **Modélisation Textuelle & Schéma Fonctionnel :**
   - Représentation du flux sous forme de liste hiérarchique détaillée ou diagramme Mermaid (`flowchart TD / LR`).

4. **Gestion des États Limites (Edge Cases) :**
   - État vide (Empty State) : comportement lorsqu'aucune donnée n'est disponible.
   - État de chargement (Loading State) : retours visuels pendant la récupération des données.
   - État d'erreur (Error State) : messages d'erreur explicites et voies de secours pour l'usager.
