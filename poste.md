# TP 1:
#### Étape  2/3 :
Version de Git estimé : 2.42
Version git : 2.56.0

#### Étape 5 :
Chemin fournis par la commande git config --global --list --show-origin :
file:C:/Users/Lilian/.gitconfig user.name=Lilian BROSSET
file:C:/Users/Lilian/.gitconfig user.email=lilian.brosset@sdvgit.fr

#### Étape 6 :
git config --global core.editor "code --wait" (pour visual studio)

#### Étape 8 :
Git utilise lilian@autre-domaine.fr
Git utilise en premier l'adresse locale

#### Étape 10 :
"git config --global core.autocrlf true" permet de gérer les fin de ligne pour évité certain problème 


git config --global --list --show-origin
file:C:/Users/Lilian/.gitconfig user.name=Lilian BROSSET
file:C:/Users/Lilian/.gitconfig user.email=lilian.brosset@sdvgit.fr
file:C:/Users/Lilian/.gitconfig init.defaultbranch=main
file:C:/Users/Lilian/.gitconfig core.editor=code --wait
file:C:/Users/Lilian/.gitconfig core.autocrlf=true

# TP 2:
#### Étape 1 :
Résultat exacte affiché par git lors d'un 'git status':
git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        pom.xml
        src/

nothing added to commit but untracked files present (use "git add" to track)

#### Étape 2 :
Avec un 'ls -a .git' 10 entrés sont affiché, " ./  ../  config  description  FETCH_HEAD  HEAD  hooks/  info/  objects/  refs/ "

#### Étape 3 : untracked/untracked
#### Étape 4 : staged/unmodified  staged/new
#### Étape 5 : staged/modified  notstaged/modified
README apparait 2 fois encore en tant que new file et modified

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

#### Étape 6 : notstaged/modified
#### Étape 7 : staged/modified reste seulement les dossiers untracked


#### Étape 9 :
La première colonne est quand les fichiers sont indexé, la deuxième ceux qui ne sont pas indexé
A : add
M : modified
?? : untracked
AM : add/modified

#### Étape 10 : 
le README.md est passé en M indexé puis après l'avoir retiré de l'indexage avec 'git restore --staged README.md' alors le README.md retourne en deuxième colonne

#### Étape 11 : 
il y a 2 commit l'ajout du README et le Complète le README 5dab800 


5dab800 (HEAD -> main) Complète le README
314913a Ajoute le README

# TP 3:

#### Étape 3 : le gitignore empêche d'indexé certain fichier

#### Étape 4 : le fichier .gitkeep est la pour que Git continue de suivre le dossier log

#### Étape 5 : la colonne index affiche i/lf et la colonne working tree affiche w/lf "i/lf    w/lf"

#### Étape 7 : 9992c8b -> 7bf6e5c
Avec la commande "git commit --amend" le message du dernier commit a pu être modifier

#### Étape 9 : il faut refaire un git add pour validé le delete

#### Étape 10 : git rm permet directement de validé la suppresion sans utilisé de git add

#### Étape 11 : Il ne laisse rien derrière car ce n'est plus suivi

#### Étape 12 : Git parle plus d'un renommage car suppression c'est delete et ajout add

#### Étape 13 : le git diff n'affiche plus rien car il n'y a plus de différence
la commande git diff --staged montre toute les modifications depuis le dernier commit

#### Étape 14 : 'git restore src/Inventaire.java

#### Étape 15 : 'git restore --staged src/Inventaire.java

#### Étape 16 :
| Je veux annuler… | Commande | Ce que je perds |
| --- | --- | --- |
| une modification non indexée | git restore | la modification |
| une indexation | git restore --staged | la dernière indexation |
| le message du dernier commit | git commit --amend | l'ancien message du commit|

#### Étape 19 : 
* 86b93b0 (HEAD -> main) arret du suivi build/sortie
* 21e3330 build/sortie.bin
* 0ab3a07 Ajout doc/notes
* 6425178 Delete brouillon
* 0c9881b brouillon 2ndtry
* c2d335a Brouillon
* 7bf6e5c Inventaire a 67