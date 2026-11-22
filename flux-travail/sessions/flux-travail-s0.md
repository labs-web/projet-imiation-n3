# Flux de Travail OpÃ©rationnel â€” Session S0 : Maquette de la Page d'Accueil

Ce document dÃ©finit le flux de travail opÃ©rationnel du **Sprint 0**.
Il est centrÃ© sur la production de son incrÃ©ment majeur : la **Maquette de la Page d'Accueil** du Blog des LaurÃ©ats.

Le flux articule de maniÃ¨re cohÃ©rente les UnitÃ©s d'Apprentissage d'ateliers pratiques (**UA-Lab**) et les UnitÃ©s d'Apprentissage d'application opÃ©rationnelle sur le projet (**UA-TÃ¢che**), totalisant **6 UAs**, **15 Ã©tapes chronologiques** et **22 tutoriels d'ingÃ©nierie**.

Les durÃ©es temporelles (80 heures / 10 jours) sont fournies Ã  titre purement indicatif pour les formateurs et le concepteur.

---

## 1. Fiche d'Identification de la Session S0

- **Identifiant :** Session S0 (Sprint 0)
- **Titre centrÃ© sur l'incrÃ©ment :** Maquette de la Page d'Accueil
- **IncrÃ©ment produit :** Maquette interactive de la page d'accueil avec son User Flow textuel, son UI Kit de composants validÃ©, et le cadrage initial du produit (Product Backlog ordonnÃ©)
- **DurÃ©e indicative :** 80 heures (10 jours ouvrÃ©s)
- **RÃ©fÃ©rentiel des compÃ©tences :** Conforme au document de rÃ©fÃ©rence [.agents/references/domaines-competences.md](../../.agents/references/domaines-competences.md)
- **Domaines de compÃ©tences et UnitÃ©s d'Apprentissage mobilisÃ©s :**
  - Domaine RÃ©alisation et Conduite de Projet (`D.351.2-realisation-projet`) :
    - UnitÃ© d'apprentissage `UA.351.21` (UA-TÃ¢che) : *Application Projet : DÃ©pÃ´t, Cadrage et Stack Technique* (Statut : **Ã€ rÃ©aliser**)
  - Domaine Scrum & Gouvernance Agile (`D.351.1-scrum`) :
    - UnitÃ© d'apprentissage `UA.351.11` (UA-Lab) : *Initiation Ã  la DÃ©marche Agile et Cadre Scrum* (Statut : **RÃ©alisÃ©e**)
  - Domaine Conception & Design Thinking (`D.311.1-design`) :
    - UnitÃ© d'apprentissage `UA.311.11` (UA-Lab) : *Design Thinking : DÃ©marche Globale et Immersion Empathique* (Statut : **Ã€ rÃ©aliser**)
    - UnitÃ© d'apprentissage `UA.311.12` (UA-Lab) : *Design Thinking : Parcours Utilisateur et Prototypage d'Interface* (Statut : **Ã€ rÃ©aliser**)
    - UnitÃ© d'apprentissage `UA.311.13` (UA-Lab) : *Design Thinking : Tests d'UtilisabilitÃ© et Validation Ergonomique* (Statut : **Ã€ rÃ©aliser**)
  - Domaine RÃ©alisation et Conduite de Projet (`D.351.2-realisation-projet`) :
    - UnitÃ© d'apprentissage `UA.351.22` (UA-TÃ¢che) : *Application Projet : Validation d'IncrÃ©ment et ClÃ´ture Agile* (Statut : **Ã€ rÃ©aliser**)
- **Objectif global d'apprentissage :**
  - Cadrer le projet initial et configurer l'espace de dÃ©veloppement Git officiel.
  - DÃ©couvrir la mÃ©thode agile Scrum et organiser la gouvernance de promotion avec le Groupe 1 en Product Owner.
  - MaÃ®triser les Ã©tapes amont du Design Thinking (Empathie, DÃ©finition) sur le cas Todo List, puis conduire l'immersion usagers et formaliser les Personas du Blog.
  - BÃ¢tir le Product Backlog initial ordonnÃ© selon MoSCoW et signer la feuille d'engagement d'Ã©quipe du Sprint 0.
  - MaÃ®triser les Ã©tapes aval du Design Thinking (IdÃ©ation, Prototypage) pour modÃ©liser le User Flow et prototyper la maquette d'accueil avec Tailwind CSS et Preline UI.
  - DÃ©couvrir les protocoles de tests d'utilisabilitÃ© et valider formellement la maquette lors de la Sprint Review 0 (Jalon Go/No-Go).

---

## 2. Organisation de la Promotion et PrÃ©requis de Lancement du Sprint 0

Pour lancer la dynamique collective du Sprint 0, l'organisation de la promotion repose sur un dÃ©coupage en 5 groupes dont les numÃ©ros reflÃ¨tent directement la prioritÃ© des missions d'ingÃ©nierie et d'accompagnement :

- **Condition d'accÃ¨s aux Groupes OpÃ©rationnels 1 Ã  4 :**  
  Pour Ãªtre affectÃ© dans l'un des groupes 1 Ã  4, chaque apprenant doit obligatoirement avoir validÃ© les **5 labs initiaux prÃ©requis fondamentaux** :
  - `lab-startup` : Prise en main de l'environnement de dÃ©veloppement et initialisation du poste.
  - `lab-markdown` : MaÃ®trise de la rÃ©daction documentaire structurÃ©e en Markdown standard.
  - `lab-marp` : Conception de diaporamas professionnels au format Marp Markdown.
  - `lab-prompt` : Formulation de prompts d'assistance et interaction avec l'Agent IA copilote.
  - `lab-presentation-pro` : Posture professionnelle et animation de soutenance technique.

- **Groupe 5 (PrioritÃ© 5 â€” PrÃ©requis Fondamentaux & Sas de Rattrapage) :**  
  Les apprenants n'ayant pas encore validÃ© l'ensemble des 5 labs initiaux sont affectÃ©s au Groupe 5. Leur prioritÃ© absolue est de finaliser et faire valider ces prÃ©requis indispensables avant d'intÃ©grer les groupes opÃ©rationnels 1 Ã  4.

- **RÃ´le OpÃ©rationnel des Groupes 1 Ã  4 (Exclusif aux Tuto-TÃ¢ches) :**  
  *RÃ¨gle mÃ©thodologique stricte :* Les groupes ne sont pas sollicitÃ©s pendant le dÃ©roulement des sÃ©ances d'UA-Lab (qui relÃ¨vent d'un apprentissage guidÃ© par le formateur). Ils interviennent pour **dÃ©bloquer et accompagner les apprenants sur les tuto-tÃ¢ches** d'application projet avant et pendant leur rÃ©alisation :
  - **Groupe 1 (PrioritÃ© 1 â€” Product Owner / Vision & Backlog) :**  
    Porte la vision mÃ©tier du *Blog des LaurÃ©ats*, priorise les User Stories initiales du Product Backlog et dÃ©bloque les arbitrages fonctionnels sur les tÃ¢ches de vision, de cadrage et de backlog. Il statue lors de la Sprint Review 0.
  - **Groupe 2 (PrioritÃ© 2 â€” Design Thinking & Prototypage) :**  
    Assure la cohÃ©rence de la dÃ©marche centrÃ©e utilisateur. Il guide et dÃ©bloque les pairs sur les tÃ¢ches d'immersion terrain, la formalisation des Cartes d'Empathie, la modÃ©lisation des fiches Personas, ainsi que sur le User Flow et les maquettes interactives.
  - **Groupe 3 (PrioritÃ© 3 â€” Cadre Scrum & Organisation Agile) :**  
    Veille Ã  la bonne appropriation du cadre Scrum. Il guide et dÃ©bloque les pairs sur la feuille d'engagement d'Ã©quipe (`sprint-0.md`) et le respect des cÃ©rÃ©monies agiles.
  - **Groupe 4 (PrioritÃ© 4 â€” Cadrage Transverse, Plan de Rapport & Diaporama) :**  
    PrÃ©pare les formats de capitalisation transverses en travaillant sur son projet fil rouge : Ã©laboration du plan type de rapport modulaire et du plan type de prÃ©sentation de soutenance Marp.

---

## 3. Cadre Tri-Projets

- **Projet d'Imitation (*Blog des LaurÃ©ats*) :** RÃ©alisation pas-Ã -pas en classe active des Ã©tapes de cadrage, d'empathie, de backlog, d'UI Kit et de la maquette de la page d'accueil.
- **Projet Technique (*Portfolio DÃ©veloppeur*) :**
  - En fin de sprint, chaque apprenant reproduit la rÃ©alisation concrÃ¨te du sprint sur son portfolio personnel (initialisation du dÃ©pÃ´t Git et maquette de sa propre page d'accueil).
  - **RÃ¨gle formelle d'exigence :** Les documents de cadrage et de conception (note de cadrage, personas, vision produit) **ne sont pas demandÃ©s** pour le portfolio dans la session. L'apprenant reste libre de les rÃ©aliser pour lui-mÃªme, mais ils ne font l'objet d'aucune Ã©valuation formelle.
- **Projet Fil Rouge (*Application MÃ©tier*, ex : Gestion de CinÃ©ma) :** Cadrage fonctionnel, formalisation des Personas et initialisation du Product Backlog de l'application mÃ©tier par les Ã©quipes projet.

---

## 4. DÃ©roulement OpÃ©rationnel des 6 UnitÃ©s d'Apprentissage (15 Ã‰tapes â€” 22 Tutoriels)

```mermaid
flowchart TD
    subgraph UA1 ["UA.351.21 (UA-TÃ¢che) : DÃ©pÃ´t, Cadrage & Stack Technique"]
        E1["Ã‰tape 1 : Initialiser le dÃ©pÃ´t Git et l'espace vitrine (T.351.211)"]
        E2["Ã‰tape 2 : Cadrer le projet d'imitation In/Out (T.351.212)"]
        E3["Ã‰tape 3 : Justifier la stack Laravel et architecture (T.351.213)"]
        E1 --> E2 --> E3
    end

    subgraph UA2 ["UA.351.11 (UA-Lab) : Initiation DÃ©marche Agile Scrum & Vision"]
        E4["Ã‰tape 4 : Ateliers Scrum sur Todo List (T.351.111 Ã  T.351.115)"]
        E5["Ã‰tape 5 : DÃ©finir la Vision Produit du Blog (T.351.116)"]
        E4 --> E5
    end

    subgraph UA3 ["UA.311.11 (UA-Lab) : Design Thinking : Empathie & Personas"]
        E6["Ã‰tape 6 : Ateliers Design Thinking & Empathie Todo List (T.311.111 Ã  T.311.113)"]
        E7["Ã‰tape 7 : Conduire l'immersion & Carte d'Empathie Blog (T.311.114)"]
        E8["Ã‰tape 8 : ModÃ©liser les Personas utilisateurs du Blog (T.311.115)"]
        E6 --> E7 --> E8
    end

    subgraph UA2_Suite ["UA.351.11 (Suite) : Product Backlog & Engagement S0"]
        E9["Ã‰tape 9 : BÃ¢tir le Product Backlog initial du Blog MoSCoW (T.351.117)"]
        E10["Ã‰tape 10 : Planifier le Sprint 0 et feuille d'engagement (T.351.118)"]
        E9 --> E10
    end

    subgraph UA4 ["UA.311.12 (UA-Lab) : Parcours Utilisateur & Prototypage Maquette"]
        E11["Ã‰tape 11 : Ateliers User Flow & UI Kit Preline Todo List (T.311.121, T.311.122)"]
        E12["Ã‰tape 12 : ModÃ©liser le User Flow textuel Accueil Blog (T.311.123)"]
        E13["Ã‰tape 13 : Concevoir l'UI Kit et Maquette Accueil Blog (T.311.124)"]
        E11 --> E12 --> E13
    end

    subgraph UA5 ["UA.311.13 (UA-Lab) : Tests d'UtilisabilitÃ© & Validation Ergonomique"]
        E14["Ã‰tape 14 : Atelier Protocoles de tests et critÃ¨res ergonomiques (T.311.131)"]
    end

    subgraph UA6 ["UA.351.22 (UA-TÃ¢che) : Validation d'IncrÃ©ment & ClÃ´ture Agile"]
        E15["Ã‰tape 15 : Valider l'IncrÃ©ment Maquette Review 0 & RÃ©trospective 0 (T.351.221)"]
    end

    UA1 --> UA2 --> UA3 --> UA2_Suite --> UA4 --> UA5 --> UA6
```

---

### UnitÃ© d'Apprentissage UA.351.21 (UA-TÃ¢che) : Application Projet : DÃ©pÃ´t, Cadrage et Stack Technique
*Domaine RÃ©alisation et Conduite de Projet (`D.351.2-realisation-projet`)*

#### Ã‰tape 1 : Initialiser le dÃ©pÃ´t Git et l'espace projet vitrine
- **Fiche Tutoriel :** `T.351.211` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 1` (`nav_order: 1`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.2-realisation-projet`
- **EntrÃ©es :** Consignes du formateur et cahier des charges initial.
- **Travail d'application sur le Blog :**
  - Cloner le dÃ©pÃ´t officiel `projet-imitation-n3`.
  - CrÃ©er et basculer sur la branche de travail dÃ©diÃ©e `sprint0`.
  - Configurer l'arborescence standard conforme Ã  `organisation-livrables.md`.
  - RÃ©diger le `README.md` racine de prÃ©sentation du produit, des objectifs et de la stack.
- **Sortie (1 livrable) :** `README.md`.

#### Ã‰tape 2 : Cadrer le projet d'imitation et rÃ©diger la note de cadrage
- **Fiche Tutoriel :** `T.351.212` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 2` (`nav_order: 2`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.2-realisation-projet`
- **EntrÃ©es :** Fiche d'expression des besoins brute du Blog des LaurÃ©ats de l'EFP.
- **Travail d'application sur le Blog :**
  - Clarifier le contexte professionnel, la problÃ©matique et les objectifs mesurables.
  - DÃ©finir les parties prenantes et leurs attentes clÃ©s.
  - Ã‰tablir la matrice de pÃ©rimÃ¨tre stricte : *In-Scope* (fonctionnalitÃ©s cibles) vs *Out-of-Scope* (exclusions formelles du MVP).
  - Identifier les contraintes rÃ©glementaires (RGPD), temporelles et d'accessibilitÃ©.
- **Sortie (1 livrable) :** `docs/cadrage/note-cadrage.md`.

#### Ã‰tape 3 : Justifier et valider le choix de la stack technologique (Laravel)
- **Fiche Tutoriel :** `T.351.213` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 3` (`nav_order: 3`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.2-realisation-projet`
- **EntrÃ©es :** Note de cadrage `docs/cadrage/note-cadrage.md`.
- **Travail d'application sur le Blog :**
  - Justifier formellement chaque brique technique retenue : Framework Backend (Laravel 13), Base de donnÃ©es (MySQL), Styling (Tailwind CSS avec Preline UI), Frontend rÃ©actif (Alpine.js), Assistance IA (Copilote Antigravity).
  - Argumenter le choix architectural face aux contraintes de maintenabilitÃ©, sÃ©curitÃ© (Policies/Gates, Spatie RBAC) et rapiditÃ© de prototypage.
- **Sortie (1 livrable) :** `docs/cadrage/stack-technique.md`.

---

### UnitÃ© d'Apprentissage UA.351.11 (UA-Lab) : Initiation Ã  la DÃ©marche Agile et Cadre Scrum
*Domaine Scrum & Gouvernance Agile (`D.351.1-scrum`)*

#### Ã‰tape 4 (Atelier 1/5) : Comprendre les principes fondamentaux et les valeurs de Scrum
- **Fiche Tutoriel :** `T.351.111` | **Type :** `tuto-atelier-notions` | **Attribut Ã©tape :** `etape: 4` (`nav_order: 1`)
- **Statut :** **RÃ©alisÃ©**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **EntrÃ©es :** Manifeste Agile (4 valeurs, 12 principes) et Guide officiel Scrum.
- **Notions fondamentales apprises :** DiffÃ©rence entre cycle en cascade et dÃ©marche empirique, piliers Scrum (Transparence, Inspection, Adaptation), rÃ´les Scrum (PO, SM, DÃ©veloppeurs), 5 Ã©vÃ©nements et 3 artÃ©facts.
- **Livrables de rÃ©fÃ©rence formateur (cas Todo List) :**
  - Fiche d'atelier : `ua-lab/scrum/initiation-scrum/comprendre-scrum/comprendre-scrum.md`.
  - Diaporama Marp : `ua-lab/scrum/initiation-scrum/comprendre-scrum/presentation-comprendre-scrum.md`.

#### Ã‰tape 4 (Atelier 2/5) : Formaliser la vision produit et cadrer les besoins utilisateurs
- **Fiche Tutoriel :** `T.351.112` | **Type :** `tuto-atelier-notions` | **Attribut Ã©tape :** `etape: 4` (`nav_order: 2`)
- **Statut :** **RÃ©alisÃ©**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **EntrÃ©es :** Principes de modÃ©lisation du besoin utilisateur.
- **Notions fondamentales apprises :** Formulation de la Vision Produit (Product Goal), structure standard d'une User Story, critÃ¨res qualitÃ© INVEST, critÃ¨res d'acceptation opÃ©rationnels.
- **Livrables de rÃ©fÃ©rence formateur (cas Todo List) :**
  - Fiche d'atelier : `ua-lab/scrum/initiation-scrum/vision-besoins/vision-besoins.md`.
  - Diaporama Marp : `ua-lab/scrum/initiation-scrum/vision-besoins/presentation-vision-besoins.md`.

#### Ã‰tape 4 (Atelier 3/5) : Concevoir et ordonner un Product Backlog selon MoSCoW
- **Fiche Tutoriel :** `T.351.113` | **Type :** `tuto-atelier-notions` | **Attribut Ã©tape :** `etape: 4` (`nav_order: 3`)
- **Statut :** **RÃ©alisÃ©**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **EntrÃ©es :** Liste brute d'exigences et techniques d'estimation agile relative.
- **Notions fondamentales apprises :** RÃ´le du Product Backlog comme rÃ©fÃ©rentiel vivant, estimation agile (Story Points, suite de Fibonacci), mÃ©thode de priorisation MoSCoW (Must, Should, Could, Won't), rituels d'affinement (Refinement).
- **Livrables de rÃ©fÃ©rence formateur (cas Todo List) :**
  - Fiche d'atelier : `ua-lab/scrum/initiation-scrum/product-backlog/product-backlog.md`.
  - Diaporama Marp : `ua-lab/scrum/initiation-scrum/product-backlog/presentation-product-backlog.md`.

#### Ã‰tape 4 (Atelier 4/5) : Planifier un Sprint et piloter l'exÃ©cution par la valeur
- **Fiche Tutoriel :** `T.351.114` | **Type :** `tuto-atelier-notions` | **Attribut Ã©tape :** `etape: 4` (`nav_order: 4`)
- **Statut :** **RÃ©alisÃ©**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **EntrÃ©es :** Product Backlog ordonnÃ© et capacitÃ© nominale d'Ã©quipe.
- **Notions fondamentales apprises :** DÃ©roulement du Sprint Planning (Partie 1 Quoi / Partie 2 Comment), formulation du Sprint Goal, dÃ©coupage des US en tÃ¢ches techniques ($\le$ 8h), suivi au Daily Scrum et pilotage par le Burndown chart.
- **Livrables de rÃ©fÃ©rence formateur (cas Todo List) :**
  - Fiche d'atelier : `ua-lab/scrum/initiation-scrum/sprint-planning-execution/sprint-planning-execution.md`.
  - Diaporama Marp : `ua-lab/scrum/initiation-scrum/sprint-planning-execution/presentation-sprint-planning-execution.md`.

#### Ã‰tape 4 (Atelier 5/5) : Conduire la Revue de Sprint et animer la RÃ©trospective d'Ã©quipe
- **Fiche Tutoriel :** `T.351.115` | **Type :** `tuto-atelier-notions` | **Attribut Ã©tape :** `etape: 4` (`nav_order: 5`)
- **Statut :** **RÃ©alisÃ©**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **EntrÃ©es :** IncrÃ©ment livrable et critÃ¨res de la Definition of Done (DoD).
- **Notions fondamentales apprises :** DÃ©monstration contradictoire en Sprint Review devant le PO, validation formelle au regard de la DoD, animation rÃ©flexive de la RÃ©trospective et engagement sur des actions concrÃ¨tes d'amÃ©lioration.
- **Livrables de rÃ©fÃ©rence formateur (cas Todo List) :**
  - Fiche d'atelier : `ua-lab/scrum/initiation-scrum/revue-retrospective/revue-retrospective.md`.
  - Diaporama Marp : `ua-lab/scrum/initiation-scrum/revue-retrospective/presentation-revue-retrospective.md`.

#### Ã‰tape 5 (TÃ¢che 1) : DÃ©finir la Vision Produit (Product Goal) du Blog des LaurÃ©ats
- **Fiche Tutoriel :** `T.351.116` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 5` (`nav_order: 6`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 1 (Product Owner)**.
- **EntrÃ©es :** Note de cadrage `docs/cadrage/note-cadrage.md`.
- **Travail d'application sur le Blog :**
  - En concertation avec le Product Owner (Groupe 1), formaliser la Vision Produit dÃ©finissant la proposition de valeur claire pour les apprenants et laurÃ©ats de l'EFP.
  - SpÃ©cifier le positionnement Ã©ditorial, la cible et les mÃ©triques de succÃ¨s stratÃ©giques.
- **Sortie (1 livrable) :** `docs/produit/vision-produit.md`.

#### Ã‰tape 9 (TÃ¢che 2) : BÃ¢tir et ordonner le Product Backlog initial du Blog (MoSCoW)
- **Fiche Tutoriel :** `T.351.117` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 9` (`nav_order: 7`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 1 (Product Owner)**.
- **EntrÃ©es :** Vision Produit `docs/produit/vision-produit.md` et fiches Personas validÃ©es `docs/analyse/personas.md`.
- **Travail d'application sur le Blog :**
  - Animer l'atelier d'expression des besoins avec le PO (Groupe 1).
  - DÃ©couper le produit en User Stories INVEST complÃ¨tes avec critÃ¨res d'acceptation testables.
  - Ordonner rigoureusement le Product Backlog selon la mÃ©thode MoSCoW (Must, Should, Could, Won't) en isolant le pÃ©rimÃ¨tre prioritaire du Sprint 1.
- **Sortie (1 livrable) :** `scrum/product-backlog.md`.

#### Ã‰tape 10 (TÃ¢che 3) : Planifier le Sprint 0 et formaliser la feuille d'engagement d'Ã©quipe
- **Fiche Tutoriel :** `T.351.118` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 10` (`nav_order: 8`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.1-scrum`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 3 (Cadre Scrum & Organisation Agile)**.
- **EntrÃ©es :** Product Backlog ordonnÃ© `scrum/product-backlog.md` et capacitÃ© de travail de la promotion.
- **Travail d'application sur le Blog :**
  - DÃ©finir l'objectif du Sprint 0 (*Sprint Goal* : production et validation de la maquette d'accueil, du User Flow et de l'UI Kit).
  - Ã‰tablir la composition des Ã©quipes et les rÃ´les (PO, Scrum Master, DÃ©veloppeurs).
  - SÃ©lectionner les User Stories et dÃ©couper les tÃ¢ches d'ingÃ©nierie opÃ©rationnelle.
  - Ã‰tablir la Definition of Done (DoD) de la maquette et signer la feuille d'engagement d'Ã©quipe.
- **Sortie (1 livrable) :** `sprints/sprint-0.md`.

---

### UnitÃ© d'Apprentissage UA.311.11 (UA-Lab) : Design Thinking : DÃ©marche Globale et Immersion Empathique
*Domaine Conception & Design Thinking (`D.311.1-design`)*

#### Ã‰tape 6 (Atelier 1/3) : DÃ©couvrir la dÃ©marche globale du Design Thinking et ses 5 phases
- **Fiche Tutoriel :** `T.311.111` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 6` (`nav_order: 1`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** MÃ©thodologie du Double Diamant (Design Council).
- **Travail d'atelier :** S'approprier les 5 phases (Empathie, DÃ©finition, IdÃ©ation, Prototypage, Test), distinguer les modes de pensÃ©e divergente et convergente.
- **Livrables attendus (sur Todo List) :**
  - Fiche d'atelier : `tutoriels/design/design-thinking-empathie/demarche-design-thinking/demarche-design-thinking.md`.
  - Diaporama Marp : `tutoriels/design/design-thinking-empathie/demarche-design-thinking/presentation-demarche-design-thinking.md`.

#### Ã‰tape 6 (Atelier 2/3) : Conduire une immersion utilisateur et formaliser la carte d'empathie
- **Fiche Tutoriel :** `T.311.112` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 6` (`nav_order: 2`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** Techniques d'observation terrain et canevas de Carte d'Empathie.
- **Travail d'atelier :** Mener l'immersion sur les usagers d'une Todo List, renseigner les 4 quadrants (Dit, Fait, Pense, Ressent) et formaliser les frustrations et gains.
- **Livrables attendus (sur Todo List) :**
  - Fiche d'atelier : `tutoriels/design/design-thinking-empathie/immersion-empathie/immersion-empathie.md`.
  - Diaporama Marp : `tutoriels/design/design-thinking-empathie/immersion-empathie/presentation-immersion-empathie.md`.

#### Ã‰tape 6 (Atelier 3/3) : ModÃ©liser les profils utilisateurs types Ã  travers les Personas
- **Fiche Tutoriel :** `T.311.113` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 6` (`nav_order: 3`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** Carte d'Empathie Todo List validÃ©e.
- **Travail d'atelier :** ModÃ©liser un Persona archÃ©typal sur Todo List (objectifs, motivations, scÃ©nario d'usage type).
- **Livrables attendus (sur Todo List) :**
  - Fiche d'atelier : `tutoriels/design/design-thinking-empathie/empathie-personas/empathie-personas.md`.
  - Diaporama Marp : `tutoriels/design/design-thinking-empathie/empathie-personas/presentation-empathie-personas.md`.

#### Ã‰tape 7 (TÃ¢che 1) : Conduire l'immersion usagers et formaliser la Carte d'Empathie du Blog
- **Fiche Tutoriel :** `T.311.114` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 7` (`nav_order: 4`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 2 (Design Thinking)**.
- **EntrÃ©es :** Vision Produit `docs/produit/vision-produit.md` et grille de recueil terrain.
- **Travail d'application sur le Blog :**
  - Mener l'immersion terrain auprÃ¨s des profils clÃ©s (apprenants en recherche d'inspiration, laurÃ©ats souhaitant partager, formateurs).
  - SynthÃ©tiser les verbatims et comportements observÃ©s dans la Carte d'Empathie du Blog.
- **Sortie (1 livrable) :** `docs/analyse/empathie.md`.

#### Ã‰tape 8 (TÃ¢che 2) : ModÃ©liser et formaliser les Personas types du Blog des LaurÃ©ats
- **Fiche Tutoriel :** `T.311.115` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 8` (`nav_order: 5`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 2 (Design Thinking)**.
- **EntrÃ©es :** Carte d'Empathie du Blog `docs/analyse/empathie.md`.
- **Travail d'application sur le Blog :**
  - Formaliser les 3 fiches Personas dÃ©taillÃ©es du Blog des LaurÃ©ats :
    - *Youssef*, apprenant en formation (besoin de retours d'expÃ©rience concrets et de conseils mÃ©thodologiques).
    - *Sara*, laurÃ©ate en poste dÃ©veloppeur web (volontÃ© de valoriser son parcours et de transmettre son vÃ©cu).
    - *Karim*, tuteur / responsable pÃ©dagogique EFP (souhait de crÃ©er du lien durable et de valoriser l'insertion des promotions).
  - SpÃ©cifier leurs objectifs prioritaires, points de friction et opportunitÃ©s fonctionnelles pour le Blog.
- **Sortie (1 livrable) :** `docs/analyse/personas.md`.

---

### UnitÃ© d'Apprentissage UA.311.12 (UA-Lab) : Design Thinking : Parcours Utilisateur et Prototypage d'Interface
*Domaine Conception & Design Thinking (`D.311.1-design`)*

#### Ã‰tape 11 (Atelier 1/2) : ModÃ©liser un User Flow et concevoir l'architecture de navigation
- **Fiche Tutoriel :** `T.311.121` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 11` (`nav_order: 1`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** ScÃ©narios d'usage d'une Todo List.
- **Travail d'atelier :** MaÃ®triser la syntaxe dÃ©clarative textuelle pour exprimer les flux utilisateurs (points d'entrÃ©e, actions utilisateur, dÃ©cisions conditionnelles, Ã©crans de sortie) appliquÃ©e au cas Todo List.
- **Livrables attendus (sur Todo List) :**
  - Fiche d'atelier : `tutoriels/design/parcours-utilisateur-prototypage/user-flow/user-flow.md`.
  - Diaporama Marp : `tutoriels/design/parcours-utilisateur-prototypage/user-flow/presentation-user-flow.md`.

#### Ã‰tape 11 (Atelier 2/2) : Concevoir un UI Kit de composants rÃ©utilisables avec Tailwind CSS et Preline UI
- **Fiche Tutoriel :** `T.311.122` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 11` (`nav_order: 2`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** Notions d'Atomic Design et bibliothÃ¨que de composants Tailwind CSS / Preline UI.
- **Travail d'atelier :** Concevoir une bibliothÃ¨que modulaire de composants d'interface sur Todo List (tokens de design, typographie, boutons, champs, alertes, cartes rÃ©utilisables).
- **Livrables attendus (sur Todo List) :**
  - Fiche d'atelier : `tutoriels/design/parcours-utilisateur-prototypage/prototypage-ui-kit/prototypage-ui-kit.md`.
  - Diaporama Marp : `tutoriels/design/parcours-utilisateur-prototypage/prototypage-ui-kit/presentation-prototypage-ui-kit.md`.

#### Ã‰tape 12 (TÃ¢che 1) : ModÃ©liser le User Flow textuel de la Page d'Accueil du Blog
- **Fiche Tutoriel :** `T.311.123` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 12` (`nav_order: 3`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 2 (Design Thinking)**.
- **EntrÃ©es :** Fiches Personas `docs/analyse/personas.md` et User Stories du Product Backlog `scrum/product-backlog.md`.
- **Travail d'application sur le Blog :**
  - ModÃ©liser en syntaxe dÃ©clarative textuelle le parcours utilisateur complet d'un apprenant visitant la page d'accueil du Blog (atterrissage sur la Hero section, parcours des articles rÃ©cents, filtrage par tag/catÃ©gorie, clic vers la fiche laurÃ©at dÃ©taillÃ©e).
  - Cartographier les Ã©tats d'erreur, les Ã©tats de chargement et les transitions interactives.
- **Sortie (1 livrable) :** `docs/conception/user-flow.md`.

#### Ã‰tape 13 (TÃ¢che 2) : Concevoir l'UI Kit et prototyper la Maquette de la Page d'Accueil
- **Fiche Tutoriel :** `T.311.124` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 13` (`nav_order: 4`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **Accompagnement :** DÃ©bloquÃ© par le **Groupe 2 (Design Thinking)**.
- **EntrÃ©es :** User Flow `docs/conception/user-flow.md` et composants Preline UI.
- **Travail d'application sur le Blog :**
  - SpÃ©cifier l'UI Kit officiel du Blog des LaurÃ©ats (palette de couleurs, typographie, boutons, badges, cartes d'articles, navbar avec logo, footer).
  - Prototyper la maquette interactive et responsive de la page d'accueil du Blog (Hero section accueillante, grille d'articles, filtres par catÃ©gorie, pied de page).
- **Sorties (2 livrables) :** `docs/conception/ui-kit.md` et `docs/conception/maquettes-sprint-1.md`.

---

### UnitÃ© d'Apprentissage UA.311.13 (UA-Lab) : Design Thinking : Tests d'UtilisabilitÃ© et Validation Ergonomique
*Domaine Conception & Design Thinking (`D.311.1-design`)*

#### Ã‰tape 14 (Atelier 1/1) : DÃ©finir et exÃ©cuter les protocoles de tests d'utilisabilitÃ© et validation ergonomique
- **Fiche Tutoriel :** `T.311.131` | **Type :** `tuto-atelier` | **Attribut Ã©tape :** `etape: 14` (`nav_order: 1`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.311.1-design`
- **EntrÃ©es :** Maquette d'accueil et grille des heuristiques ergonomiques de Nielsen / Bastien & Scapin.
- **Travail d'atelier :**
  - DÃ©finir un protocole d'Ã©valuation ergonomique standardisÃ© (scÃ©narios de test, critÃ¨res de succÃ¨s, mesure du temps et des erreurs).
  - ExÃ©cuter une session de test guidÃ©e et formaliser la grille d'Ã©valuation des critÃ¨res d'utilisabilitÃ© (guidage, charge de travail, contrÃ´le explicite, adaptabilitÃ©, gestion des erreurs).
- **Livrables attendus (mÃ©thodologie gÃ©nÃ©rale) :**
  - Fiche d'atelier : `tutoriels/design/tests-utilisabilite/tests-utilisabilite-ergonomie/tests-utilisabilite-ergonomie.md`.
  - Diaporama Marp : `tutoriels/design/tests-utilisabilite/tests-utilisabilite-ergonomie/presentation-tests-utilisabilite-ergonomie.md`.

---

### UnitÃ© d'Apprentissage UA.351.22 (UA-TÃ¢che) : Application Projet : Validation d'IncrÃ©ment et ClÃ´ture Agile
*Domaine RÃ©alisation et Conduite de Projet (`D.351.2-realisation-projet`)*

#### Ã‰tape 15 : Valider l'IncrÃ©ment Maquette (Sprint Review 0 Go/No-Go) et animer la RÃ©trospective 0
- **Fiche Tutoriel :** `T.351.221` | **Type :** `tuto-tache` | **Attribut Ã©tape :** `etape: 15` (`nav_order: 1`)
- **Statut :** **Ã€ rÃ©aliser**
- **Domaine de compÃ©tence :** `D.351.2-realisation-projet`
- **Accompagnement :** ArbitrÃ© par le **Groupe 1 (Product Owner)** pour la Review et facilitÃ© par le **Groupe 3 (Cadre Scrum)** pour la RÃ©trospective.
- **EntrÃ©es :** Note de cadrage, Product Backlog initial, UI Kit, maquette interactive de la page d'accueil, retours de tests ergonomiques et engagement `sprints/sprint-0.md`.
- **Travail d'application sur le Blog :**
  - Animer la sÃ©ance de dÃ©monstration contradictoire de la maquette devant le Product Owner (Groupe 1) et les parties prenantes.
  - Auditer rigoureusement les critÃ¨res de la Definition of Done (DoD) de la maquette.
  - Prononcer la dÃ©cision collÃ©giale Go/No-Go autorisant le lancement du Sprint 1 (Delivery applicatif Laravel).
  - Mener la rÃ©trospective rÃ©flexive d'Ã©quipe sur le dÃ©roulement du Sprint 0 et formaliser 2 engagements d'amÃ©lioration continue.
- **Sorties (2 livrables) :** `sprints/pv-review-0.md` et `sprints/retrospective-0.md`.
