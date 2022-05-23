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




# New problems

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



### Git basics 2/2
* **`git log`** show all commits in the current branch’s history
* **`git show [SHA]`** show any object in Git in human-readable format
* **`git diff`** diff of what is changed but not staged
* **`git diff --staged`** diff of what is staged but not yet committed
* **`git mv [existing] [new]`** change an existing file path and stage the move

Empty subdirectories cannot be tracked. Create dummy files to work around this problem or .gitkeep



### Exercice
- config git
- create repo
- add all files
- initial commit
- change
- add change
- delete
- commit delete
- view commits
- change
- view diff
- commit




### Best Pratices

* Explain your commits completely
* Don't comment out code
* Only store the canonical stuff
* Group your commits logically




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




# Don't comment out code



### Recover files

* **`git checkout [SHA|branch] -- [file]`** Discard changes in the working directory
* **`git reset --hard [SHA]`** The staged snapshot and the working directory are both updated to match the specified commit.
* **`git revert [SHA]`** revert the changes that the related patches introduce, and record some new commits that record them
* **`git commit --amend`** lets you modify your last commit

 Be cautious when using --amend on commits shared with other team members. Amending a commit that is shared with another user will potentially require confusing and lengthy merge conflict resolutions.
<!-- .element: class="small" -->



### EXO
- change
- new file
- reset --hard
- add file
- commit
- add file
- commit
- add file
- commit
-- revert commit#2
-- checkout file from commit#1




# Only store the canonical stuff



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



### EXO
add .gitignore
add password file
commit
repeat for temporary files



# Group your commits logically
branch
(* interactive stage later)



### Work on different features / bugs

* **`git branch`** list your branches.
* **`git branch [branch-name]`** create a new branch at the current commit
* **`git checkout [branch-name]`** switch to another branch and check it out into your working directory
* **`git checkout -b [branch-name]`** create a new branch and check it out
* **`git merge [branch-name]`** merge the specified branch’s history into the current one



# exo branch and merge
create branch
checkout branch
commit
commit
switch to master
merge branch
create branch2
commit
checkout master
commit
merge branch2
list branch
delete branch2





# Git flow

* **`git tag [tag-name]`** tag the current commit with a name



https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

main
develop
features/
release/
hotfix/




### TEMP commits

* **`git stash`** save modified and staged changes
* **`git stash list`** list stack-order of stashed file changes
* **`git stash pop`** write working from top of stash stack
* **`git stash drop`** discard the changes from top of stash stack
* **`git stash apply`** apply the changes from top of stash stack



# EXO
- create files
- switch branch
- stash
switch branch
create branch
apply
apply
list
pop

