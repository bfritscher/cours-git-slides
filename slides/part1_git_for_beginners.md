63-21.2 - Atelier d'approfondissement de la programmation
<!-- .element style="font-size:0.7em;margin:4em 0;" -->

# Workshop GIT

![](images/common/logo_heg.png)
<!-- .element style="position:absolute; top:0; left:0;width:40%;" class="nopdf" -->

![](images/common/logo_hes-so.jpg)
<!-- .element style="position:absolute; top:0; right:0;width:10%;" class="nopdf" -->

[Boris.Fritscher@he-arc.ch](mailto:Boris.Fritscher@he-arc.ch)
<!-- .element style="position:absolute; bottom:20px; left:0;" class="nopdf" -->

#### Part 1: Git for Beginners

#### *Introduction to a Version Control System*




## After days of coding

* Editing code and making backups
* Commenting out code

-> Need for a version control system

![](images/code_quality_wtf.png)<!-- .element: class="bottom right" -->




### Have you ever:

* Made a change to code, realised it was a mistake and wanted to revert back?
* Had to maintain multiple versions of a product?
* Wanted to see the difference between two (or more) versions of your code?
* Wanted to prove that a particular change broke or fixed a piece of code?
* Wanted to review the history of some code?
* Wanted to submit a change to someone else's code?
* Wanted to share your code, or let other people work on your code?
* Wanted to see how much work is being done, and where, when and by whom?
* Wanted to experiment with a new feature without interfering with working code?

<!-- .element: class="small" -->

https://stackoverflow.com/questions/1408450/why-should-i-use-version-control

<!-- .element: class="credits" -->




# Why use a VCS

* Storing Versions (Properly)
* Reverting Changes
* Branching (experiment, work on different features)
* Collaboration (conflict resolution)
* Understanding What Happened




### Centralized VCS

![](images/vcs-centralized.png)<!-- .element: class="w-75" -->

<!-- .element: class="center" -->



### Distributed VCS like Git

![](images/vcs-distributed.png)<!-- .element: class="w-50" -->

<!-- .element: class="center" -->



### Distributed VCS Advantages

* FAST
* OFFLINE (fix/commit multiple operations)
* Geography
* Flexible Workflows
* Easier Merging
* Implicit Backup
* Scale out, not just up

*Disadvantages: no Locks, Disk space*

http://ericsink.com/vcbe/html/dvcs_advantages.html

<!-- .element: class="credits" -->




# Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Download on [git-scm.com](https://git-scm.com/download/win)

[cheatsheet](https://training.github.com/)



### Git Configuration

* **`git config --global user.name "[firstname lastname]"`** credit when review version history
* **`git config --global user.email "[valid-email]"`** id for commit
* **`git config --global color.ui auto`** command line coloring
* **`git config --global init.defaultBranch main`** set the name of the default branch

<!-- .element: class="small" -->




### Git lifecycle

![](images/git-lifecycle.png)

http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository

<!-- .element: class="credits" -->




### Git basics 1/2
* **`git init`** create a new local git repository
* **`git status`** show modified files in working directory, staged for your next commit
* **`git add [file]`** add a file as it looks now to your next commit (stage)
* **`git reset [file]`** unstage a file while retaining the changes in working directory
* **`git rm [file]`** delete the file from project and stage the removal for commit
* **`git commit -m [descriptive message]`** commit your staged content as a new commit snapshot

<!-- .element: class="small" -->



### Git basics 2/2
* **`git log`** show all commits in the current branch’s history
* **`git show [SHA]`** show any object in Git in human-readable format
* **`git diff`** diff of what is changed but not staged
* **`git diff --staged`** diff of what is staged but not yet committed
* **`git mv [existing] [new]`** change an existing file path and stage the move

<!-- .element: class="small" -->

Empty subdirectories cannot be tracked. Create dummy files to work around this problem or .gitkeep



### Exercice: Git Basics
1. Configurer votre nom prénom et email dans git
2. Créer un nouveau dossier contenant un fichier texte `todo.txt` et versionner ce fichier avec un commit git nommé `initial commit`.
3. Ajouter une ligne `"- acheter du lait"` dans le fichier `todo.txt` et créer un fichier `vacances.txt`. Ajouté uniquement ce nouveau fichier au staging.
4. Commiter avec le message `projet de vacances`, puis commiter votre fichier todo.txt
5. A l'aide de commandes git trouvez la différence entre ces deux fichiers: [words1.txt](files/words1.txt) [words2.txt](files/words2.txt) (possible avec ou sans commit)

<!-- .element: class="small" -->

[Quiz](https://forms.office.com/Pages/ResponsePage.aspx?id=fX07WxnhBU2QIvd18uSOlnwGT4lx77ZFo6AQM_5Ntr9UNTg2MzgxUUgzSjNLV1lNUFJBQ0ZCQlI0Mi4u)




### Best Pratices

* Explain your commits completely
* Don't comment out code
* Only store the canonical stuff
* Group your commits logically

🥇

<!-- .element: style="font-size: 80pt;margin-top:1em;text-align:center" -->




### Explain your commits completely

![](images/xkcd-commits.png)
https://xkcd.com/1296/

<!-- .element: class="credits" -->



### Do Your Commit Messages Suck?

<iframe width="640" height="480" src="https://www.youtube.com/embed/8YjSty6bfog?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

https://www.youtube.com/watch?v=8YjSty6bfog

<!-- .element: class="credits" -->



### Conventional Commits

https://www.conventionalcommits.org/fr/v1.0.0/

* Automatically generating CHANGELOGs.
* Automatically determining a semantic version bump (based on the types of commits landed).
* Communicating the nature of changes to teammates, the public, and other stakeholders.
* Triggering build and publish processes.
* Making it easier for people to contribute to your projects, by allowing them to explore a more structured commit history.




### Don't comment out code

![](images/dead-code-01-2x.png)



### Recover files

* **`git checkout [SHA|branch] -- [file]`** Discard changes in the working directory
* **`git reset --hard [SHA]`** The staged snapshot and the working directory are both updated to match the specified commit.
* **`git revert [SHA]`** revert the changes that the related patches introduce, and record some new commits that record them
* **`git commit --amend`** lets you modify your last commit

 Be cautious when using --amend on commits shared with other team members. Amending a commit that is shared with another user will potentially require confusing and lengthy merge conflict resolutions.
<!-- .element: class="small" -->



### Exercice: Git undo

0. Créer un repository git avec un fichier `todo.txt` qui contient 3 commits (un nouveau changement par ligne dans le fichier)
1. Supprimer le fichier `todo.txt` et créer un fichier `todo.encrypted`. Comment remettre tout l'espace de travail dans l'état du dernier commit?
2. Ajouter un commit qui ajoute le texte suivant dans le `todo.txt` : `- acheter du lait` puis faire un autre commit qui ajoute un nouveau fichier `voitures.txt`. On veut annuler le changement apporté par le commit `- acheter du lait` comment le faire avec git?
3. Finalement on veut remplacer la version actuel du fichier `todo.txt` par la version du dernier commit de l'étape 0. Comment faire?

<!-- .element: class="small" -->

[Quiz](https://forms.office.com/Pages/ResponsePage.aspx?id=fX07WxnhBU2QIvd18uSOlnwGT4lx77ZFo6AQM_5Ntr9UQ0pTQkZHS0ozVEdBWlJFQkxCTVdYRzNQRS4u)




# Only store the canonical stuff

![](images/hoarding_vs_collecting.jpg)


### .gitignore

.gitignore tells git which files (or patterns) it should ignore. It's usually used to avoid committing transient files from your working directory that aren't useful to other collaborators, such as compilation products, temporary files IDEs create, etc.
<!-- .element: class="small" -->

- \* is used as a wildcard match
- \# is used to add comments to a .gitignore file

<!-- .element: class="w-40 left" -->

```
# Ignore Mac system files
.DS_store

# Ignore node_modules folder
node_modules

# Ignore all text files
*.txt

# Ignore files related to API keys
.env
```
<!-- .element: class="w-50 right" -->

http://git-scm.com/docs/gitignore

<!-- .element: class="credits" -->



### Exercice .gitignore

1. Créer un dossier git `top secret` et y mettre un fichier `vacances.txt` avec votre `initial commit`
2. Créer un fichier `.gitignore` et `password.txt` et faite en sorte que `password.txt` soit ignoré par git
3. Vérifier en faisant un changement dans `vacances.txt` et un commit.
4. Modifier le fichier `.gitignore` pour qu'il ignore les fichiers se termninant par l'extention `.tmp`
5. Vérifier en faisant un add et commit après avoir crée les fichiers `file1.tmp`, `file2.tmp` et un fichier `file3.tmp` dans un dossier `images`

<!-- .element: class="small" -->




# Group your commits logically

* branches
* (interactive staging)



### Work on different features / bugs

* **`git branch`** list your branches.
* **`git branch [branch-name]`** create a new branch at the current commit
* **`git checkout [branch-name]`** switch to another branch and check it out into your working directory
* **`git checkout -b [branch-name]`** create a new branch and check it out
* **`git merge [branch-name]`** merge the specified branch’s history into the current one
* **`git log --oneline --graph --decorate`** show the history of your commits with a graph

<!-- .element: class="small" -->



### Exercice:  git branch and merge

0. Créer un repository git avec un fichier `todo.txt` qui contient 3 commits (un nouveau changement par ligne dans le fichier)
1. Créer une branche `vacances` et y mettre un fichier `vacances.txt`
2. Ajouter deux commits qui change le fichier `vacances.txt`
3. Faire un merge de la branche `vacances` dans la branche `main`
4. Répéter l'opération pour une branche `voiture`
5. Comment afficher les branches qui exsite?
6. A quoi ressemble le graph de commits?
7. Comment supprimer les branches `vacances` et `voiture`?

<!-- .element: class="small" -->




# Git Tag

* **`git tag [tag-name]`** tag the current commit with a name

<img src="images/01 How it works.svg" />

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

<!-- .element: class="credits" -->




# Git Flow Concepts

* **main** official release history branch
* **develop** branch for integrating features
* **feature/** branch to develop a feature
* **release/** branch to release a set of features, while development continues on *develop*
* **hotfix/** maintenance branch, only branch allowed from *main*



### Feature branches

<img src="images/02 Feature branches.svg" style="width: 80%" />

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

<!-- .element: class="credits" -->



### Release branches

<img src="images/03 Release branches.svg" style="width: 80%" />

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

<!-- .element: class="credits" -->



### Hotfix branches

<img src="images/04 Hotfix branches.svg" style="width: 80%"/>

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

<!-- .element: class="credits" -->




### Temporary commits (Stash Files)

* **`git stash`** save modified and staged changes
* **`git stash list`** list stack-order of stashed file changes
* **`git stash pop`** write working from top of stash stack
* **`git stash drop`** discard the changes from top of stash stack
* **`git stash apply`** apply the changes from top of stash stack



# Exercice Git-Katas Basic-Stashing

https://github.com/eficode-academy/git-katas

