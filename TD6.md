# TD6 : Git Filesystem & Commits

## Exercise 1: Configure Git
Cette partie est fait automatiquement sur Github

```
git
git config -h
git config --global user.name "Linda HE"
git config --global user.email "linda.he@edu.devinci.fr
git config --list
```
## Exercise 2 : Basic workflow with a single file
```
mkdir course2023
cd course 2023
git init
ls -A
git status
echo "# Test repository" > readme.md
cat readme.md
git status #il y a des untracked files : il faut ajouter les fichiers dans git
git add readme.md
git status #nouveau fichier dans la stage zone
git commmit -m "Add readme file"
git status
git branch
git log  #affciche les commits dans l'ordre chronologique
git log --pretty=oneline #pareil que log mais plus facile à lire car pas date, utilisateur
```
## Exercise 3 : Basic workflow with multiple files treated separately
```
cd course2023
>main.py
>function.py
git status
#Ajout et commit de main.py d'abord puis de function.py
git add main.py
git status
git commit -m "Add main file"
git add function.py
git status
git commit -m "Add function file"
git log --oneline
```

## Exercice 4 : Basic workflow with multiple files treated all at once
```
> requirements.txt
> .gitignore
> .private
git status
git add . #ajoute tous les fichiers en même temps
git commit -m "Add standard repo files" #commit va creer un seul msg pour les 3 fichiers ensemble
git status
git log-oneline
```

## Exercise 5 : Private files
--> Comment gérer des fichiers privés
```
cd course2023
echo "temp.ipynb" >> .gitignore
> temp.aux
> temp.log
git status
# mettre temp* dans .gitignore pour ignorer tous les fichiers commençant par temp
echo *.private* >> exclude
echo *boxing* >> .git/info/exclude
```

## Exercise 6: Difference between versions
```
vim readme.md
# on écrit par exple "This is for training" dans le fichier
cat readme.md
git add readme.md
git diff --staged
git commit - m "Add description"
git diff # rien ne s'affiche
vim readme.md
# on modifie "This is just for training"
git diff #cette fois affiche la ligne qui a été supprimé et celle ajouté (en gros modifié)

```
## Exercise 7: Undo
```
cd course2023
git status
rm * #supprime tout
ls #il y a plus rien
git restore .
ls #on restore nos fichiers SAUF les fichiers temp 

mkdir backup
cp -r .git backup
rm -rf course2023 
cd backup
git restore.
```
Modifier des fichiers mis dans la stage zone
```
git add readme.md
git restore --staged readme.md
git status
git commit -am "Add interesting stuff" #commit et add les fichiers modifiés (trackés par git)
git checkout HEAD~ #on va au commit précédént mettre ~2 ~3 pour encore avant
git log --all --graph #visualise ensemble des graphs des commits
git checkout master #revenir à la dernière version
git checkout HEAD~2 #reviens à 2 commits avant
ls
git checkout 8d1b3 #direct avec le nom du commit 
```
