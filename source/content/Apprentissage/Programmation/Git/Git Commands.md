---
tags:
  - coding/git
---

#### Lancer un projet et le commit
```shell
cd ~/Documents         # Accédez à Documents
mkdir MonNouveauProjet  # Crée un nouveau dossier MonNouveauProjet
cd MonNouveauProjet # Entrez dans le dossier
git init # Initialise un dépôt Git
touch README.md # Crée un fichier README.md
echo "Mon projet Git" > README.md  # Ajoute du texte
git add . # Ajoute les fichiers au suivi
git commit -m "Initial commit"  # Valide le projet
git push origin main

```

##### Explication des commandes de bases
- Pour vérifier le status d'un ficher: `git status`
	- SI rouge: alors non index
	- Si Verte: alors index

###### le set up
-> [[set up Git et GitGHub]]
``mdir``: pour créer un dossier


`git init` lets you initialize Git in your folder.

```shell
touch README.md
```
Permet de créer fichier dans l'ordinateur, *.md mais peux aussi être n'importe quel type de fichier.*


`git remote add origin` finally connects the local folder to the repository on GitHub. It is followed by the repository's link.

###### Déplacement dans les ficher
``cd``: Change Directory in the [[terminal - cmd]], pour ce déplacer dans les folders. 
`d ~/Documents`
- `~` is a shortcut for your home directory (e.g., `C:/Users/YourUsername`).

savoir ou je suis !!!
```shell
pwd
```


##### Pour arriver au commit
- [ ] *on vient de modifier un fichier*

>[!info] STEP
>**modifier → ajouter → committer → pousser**.


`git add .` pour ajouter des fichiers ou des **modifications** à la zone de staging (index).
OU 
un fichier particulier
```bash
git add nom_du_fichier
```

`git commit` stores the added files. Use `-m` for message followed by the actual message.
```shell
git commit -m "Ajout du fichier index.html"``
```


`git push -u origin main` pushes the code to GitHub. The `-u` flag creates a tracking reference for the branch, and `origin main` puts the code in the `main` branch.
OU 
**Envoyer les modifications vers le dépôt distant**:
```bash
git push origin nom_de_la_branche
```



###### Les branches
`git branch NewBranch` creates a new branch which is a new version of the repository as it appears when added.

Créer une nouvelle branche
```shell
git branch NouvelleBranche
```

Changer de branche :
```bash
git checkout nom_de_la_branche
```

`git branch`;  l'étoile \* donne la branche sur laquelle on est.


Intégrer la nouvelle branch
``` shell
git merge NouvelleBranche
```

----
 Créer une nouvelle branche et changer de branch directement:   
```bash  
git checkout -b nouvelle_branche
```


### Command situationnel

- ``git branch -d`` permet de supprimer une branche.
- ``git status`` permet de voir l’état des fichiers.
- ``git stash`` enregistre les modifications non indexées pour une utilisation ultérieure. -> [[Stash]]
- ``git log ``affiche l'historique des commits réalisés sur la branche courante.
- ``git reset --hard HEAD^`` permet de réinitialiser l'index et le répertoire de travail à l'état du dernier commit.
- ``git commit --amend ``permet de sélectionner le dernier commit pour y effectuer des modifications.



> Gardez à l'esprit que   `git revert`  sert à annuler des changements commités, tandis que   `git reset HEAD`   permet d'annuler des changements non commités.


**Attention**:   `git revert`  peut écraser vos fichiers dans votre répertoire de travail, il vous sera donc demandé de "commiter" vos modifications ou de les remiser.

###### Gestion des versions quand une équipe
- [[Journalisation de Git]]
- [[Git Reset]]
- [[Git revert]]
- [[Git Blame]]

#### Commande très situationnel

###### Configurer paramètre de [[Git]]
`--global`: effectue une modification pour tout les projets. 

`git config --list`   pour voir la liste des paramètres qui ont été modifier. 


# more info sur chaque command

###### touch
- **`touch`** est une commande système (Unix/Linux et Git Bash sur Windows) qui permet de **créer un fichier vide** s'il n'existe pas.
- Si le fichier existe déjà, `touch` met simplement à jour sa **date de modification**.

> `touch` est une commande **hors de Git**, elle agit uniquement sur votre système de fichiers local.


###### add
- **`git add`** est une commande Git utilisée pour **ajouter des fichiers ou des modifications** à la **zone de staging** (index).
- Cela prépare les fichiers pour le prochain **commit**

>  `git add` fait partie de Git. Il **n'affecte pas les fichiers**, mais les prépare pour être **enregistrés** (commit) dans l'historique Git.



###### -m 
 -m (comme message) est ce qu'on appelle un **argument**, qui est ajouté à la commande principale. Ici "-m" permet de définir un message particulier rattaché au commit effectué. Si vous n’utilisez pas cet argument, la commande “git commit” ouvrira un éditeur de texte dans lequel vous pourrez saisir le message de commit.



###### commit
La commande `commit` enregistre les modifictions en local seulement ! Maintenant il faut push les modifications.