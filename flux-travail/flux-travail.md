# Flux de travail du projet 


## Introduction 
Ce document, documenter et rapporter les étape de travail afin de noter tous les étape de réalisation de projet, afin de tracer un flux de travail de réalisation de Projet d'imitation de n3. 

Aprés l'analys de flux de travail on peut donner deux livrable : 

- Flux de travail pour la réalisation de projet d'imitation
- Flux de travail de pour la réalisation de projet technique 
- Flux de travail pour la réalisation de projet file rouge.

puisque les trois proche se réaliser en suivant les les même méthode et processus de développemet 

- 2TUP
- Dégine thinking
- Conception Oprienté objet avec UML
- Agiel - Scrum

en suivan, les étape déja réaliser dans notre projet : 



## Création et initialisation de Projet 


- Créer le projet 
- git init
- Création de fichier README.md qui contient la description de projet.

### Livrable 
- Dépôt github
- README.md


##  Création de prompt-creator.prompt.md 


### Pré-repquis d'apprentissage 

Réalisation de lab : Prompt-Engineering 

Ce lab permet  à l'apprenant de savoire comment écrie des prompt, selon la méthode RIO.


### Travail à réaliser


on va créer au début le prompt : /prompts/1.init-projet.prompt.md, 
puis aprés sa validation on va créer le prompt : /prompt/prompt-creator.prompt.md
- 


Créer le prompt qui permet de réaliser : init-projet 



Création d'un prompt qui permet d'initialisation un projet avec le fichier READE.md 

- input : fichier READE.md qui contient la description et le contexte de projet 
- output : Fichie READE.md : clean et reformuler selon la strcutre valide
- règle : 
  - Le niveau de français A1
  - Utilisation des mots technique profesionnelle de développeur, même si le niveau est A1



### Livrable 

/prompts/1.init-projet.prompt.md
/prompt/prompt-creator.prompt.md



## Comment et noter les étape de Flux de travail 

### Travail réalisé
Documentation de flux de travail, noter chaque étape de réalisation de projet en noter les élément suivant : 

- Travail réalisé
- Livrable 

### Livrable 
- Livrable : docs/flux-travail.md



## Création de prompt pour chaque étape de flux de travail 

Pour chaque étape de flux de travail, l'apprenant est amené à créer un prompt pour que l'IA soit capable de réaliser les livrables d'un flux de travail.

### Règles pour concevoir un prompt :
- **Nommage** : Chaque étape doit avoir un slug et le fichier doit se terminer par `.prompt.md` (format : `[numéro].[slug].prompt.md`).
- **Compacité stricte** : Le prompt doit être le plus compact possible, uniquement pour expliquer la règle et la consigne à l'IA, sans texte superflu.
- **Généricité** : Le prompt doit être générique et applicable à tout projet informatique.
- **Format Markdown sans tableau** : Utiliser exclusivement des listes à puces pour faciliter la modification par l'apprenant.
- **Liens relatifs** : Interdiction des liens absolus, utiliser uniquement des liens relatifs.
- **Indexation** : Ajouter le prompt dans `prompts/prompts-index.yml` avec son `name` et sa `description`.

### Livrable 
- `prompts/README.md`
- `prompts/prompts-index.yml`
- `prompts/[slug].prompt.md`



## 3. Création et Planificiation des issues 

Pendant la réalisation de projet on peut avorie des tâche qui ne sont pas suive par l'application Active LMS. ou l'apprenant veul créer des tâche ou le chef de projet a demande un travail qui n'est pas suivant par l'application Active LMS. dans ce cas l'apprenant est amenier à créer des issues. 

ces issues doit être valider par le formateur avant de les déposer dnas le dépôt github. 

###  Livrable 

- issues/README.md
- isses/issues-closes
- issues/issues-à-valider.md
- issues/issues-open.md


