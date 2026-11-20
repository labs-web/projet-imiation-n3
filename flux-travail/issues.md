## Phase 1 : Sprint 0 — Cadrage, Design Macro et Socle Technique

Ce Sprint initial est limité dans le temps (*timebox* courte de 3 à 10 jours selon la taille du projet). Il produit un **socle validé** prêt pour le développement, sans maquetter toute l'application.

| Étape | Phases de référence | Description | Input | Output |
| --- | --- | --- | --- | --- |
| **1. Planifier le Sprint 0** | **Scrum** (Sprint Planning 0) / **GP** (Initialisation) | Fixer la durée fixe (*timebox*) du Sprint 0, les objectifs de cadrage et la liste des livrables attendus à la Review 0. | Idée initiale ou demande client. | Plan et objectifs du Sprint 0. |
| **2. Cadrer le projet et comprendre l'utilisateur** | **GP** (Initialisation) / **DT** (Empathie) | Définir le périmètre, les contraintes (délai, budget, technique) et recueillir les besoins réels sur le terrain. | Demande client et contexte métier. | Note de cadrage et profils utilisateurs (Personas / besoins clés). |
| **3. Définir la Vision et le Product Backlog initial** | **DT** (Définition) / **Dev OO** (Analyse) / **Scrum** (Backlog) | Formuler le problème central, la Vision Produit et rédiger les premières User Stories avec critères d'acceptation, classées par priorité. | Note de cadrage et observations terrain. | **Vision Produit** et **Product Backlog** initial priorisé. |
| **4. Créer la Charte Graphique et les maquettes ciblées** | **DT** (Idéation, Prototypage, Test) / **Dev OO** (Conception UI) | Réaliser : (1) un mini UI Kit (couleurs, polices, composants de base), (2) un parcours global léger (*User Flow*) du MVP, (3) les **maquettes détaillées du Sprint 1** (+ écrans à risque UX) et les tester rapidement. | Vision Produit et haut du Product Backlog. | **Charte graphique (UI Kit)**, *User Flow* global et **maquettes validées du Sprint 1**. |
| **5. Concevoir l'architecture et préparer l'environnement** | **Dev OO** (Conception & Implémentation) / **GP** (Planification) | Choisir la stack technique, esquisser le modèle de données de base (MCD / diagramme de classes), initialiser Git, le framework et la base de données. | Product Backlog initial et maquettes du Sprint 1. | Dossier d'architecture de base et **socle technique opérationnel** (projet prêt à coder). |
| **6. Valider le socle (Sprint Review 0)** | **Scrum** (Sprint Review) / **GP** (Validation / Jalon Go-No-Go) | Présenter au client/commanditaire la Vision, le Backlog, la **charte graphique**, les **maquettes du Sprint 1** et le socle technique pour obtenir le feu vert. | Livrables des étapes 3, 4 et 5. | **Socle de démarrage validé** (US du Sprint 1 officiellement *Ready*). |
| **7. Clôturer le Sprint 0 (Sprint Retrospective 0)** | **Scrum** (Sprint Retrospective) / **GP** (Amélioration continue) | Faire un bilan rapide de la collaboration et de l'environnement technique avant de lancer le premier Sprint de développement. | Vécu du Sprint 0. | Ajustements d'organisation pour le Sprint 1. |

---

## Phase 2 : Cycle Itératif Dual-Track — Sprint $N$ ($N \ge 1$, à répéter)

Deux pistes avancent en parallèle : **Delivery** (coder et livrer le Sprint $N$) et **Discovery / Refinement** (préparer les maquettes des prochaines US prioritaires du Product Backlog pour qu'elles soient *Ready* au Sprint $N+1$, sans faire le Sprint Planning à l'avance).

| Étape | Piste | Phases de référence | Description | Input | Output |
| --- | --- | --- | --- | --- | --- |
| **8. Planifier le Sprint $N$ (Sprint Planning)** | **Delivery** | **Scrum** (Sprint Planning) / **GP** (Planification) | Piocher officiellement parmi les User Stories déjà *Ready* (maquetées), fixer le *Sprint Goal $N$* et découper en tâches techniques. | Product Backlog affiné (*Ready*) + actions de la Rétrospective $N-1$. | **Sprint Goal $N$** et **Sprint Backlog $N$**. |
| **9. Concevoir en détail et développer** | **Delivery** | **Dev OO** (Conception & Implémentation) / **GP** (Exécution) | Affiner la conception technique (classes, migrations, contrôleurs, API, vues) pour les US du Sprint $N$ et écrire le code correspondant. | Sprint Backlog $N$, maquettes validées et architecture. | Code source des fonctionnalités du Sprint $N$. |
| **10. Affiner le Backlog et maquetter (Backlog Refinement / Discovery)** | **Discovery** *(En parallèle, ~10 % du temps)* | **DT** (Idéation, Prototypage, Test) / **Scrum** (Backlog Refinement) | Prendre les 2 ou 3 User Stories candidates en haut du Product Backlog (pour $N+1$), clarifier les règles, créer et tester leurs maquettes (sans engagement de Sprint). | Haut du Product Backlog (US candidates pour $N+1$) et UI Kit. | Maquettes validées et **US *Ready*** pour le futur Sprint Planning $N+1$. |
| **11. Suivre l'avancement (Daily Scrum)** | **Delivery & Discovery** | **Scrum** (Daily Scrum) / **GP** (Suivi & Maîtrise) | Point quotidien de 15 min : avancement du Sprint Backlog $N$, synchronisation avec la piste Discovery et levée des blocages. | État du Sprint Backlog $N$ et avancement Discovery. | Plan quotidien ajusté et blocages traités. |
| **12. Tester et valider l'Incrément** | **Delivery** | **Dev OO** (Tests & Validation) / **Scrum** (Definition of Done) | Exécuter les tests (unitaires, fonctionnels et non-régression) face aux critères d'acceptation du Sprint $N$. | Code du Sprint $N$ et critères d'acceptation. | **Incrément $N$** stable, testé et potentiellement livrable. |
| **13. Présenter et inspecter (Sprint Review $N$)** | **Delivery → Discovery** | **Scrum** (Sprint Review) / **DT** (Empathie & Test) / **GP** (Recette) | Faire la démo de l'Incrément $N$ aux utilisateurs/clients, valider les US terminées et ajuster les priorités du Product Backlog selon les retours. | Incrément $N$ fonctionnel. | Incrément $N$ validé et **Product Backlog mis à jour**. |
| **14. Améliorer le processus (Sprint Retrospective $N$)** | **Processus** | **Scrum** (Sprint Retrospective) / **GP** (Amélioration continue) | Analyser la méthode de travail (rythme Delivery, qualité de préparation Discovery, blocages techniques) et définir 1 à 2 actions d'amélioration. | Vécu et indicateurs du Sprint $N$. | Plan d'actions d'amélioration pour le Sprint $N+1$. |

---

## Phase 3 : Livraison et Clôture

| Étape | Phases de référence | Description | Input | Output |
| --- | --- | --- | --- | --- |
| **15. Déployer en production** | **Dev OO** (Déploiement & Maintenance) / **GP** (Exécution) | Mettre l'application en ligne sur l'environnement cible, vérifier son fonctionnement en conditions réelles et livrer la documentation. | Dernier Incrément validé. | Application en production et documentation (technique / utilisateur). |
| **16. Clôturer le projet** | **GP** (Clôture) | Valider officiellement la réception du projet avec le client, archiver les livrables et capitaliser sur les leçons apprises. | Application déployée et bilans des Sprints. | PV de recette / Bilan final de projet. |

---

Souhaitez-vous que je traduise ce flux complet en un **diagramme Mermaid** pour visualiser clairement le Sprint 0, les deux pistes parallèles (*Delivery* / *Discovery*) et la boucle des Sprints ?