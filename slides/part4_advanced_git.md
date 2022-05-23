63-21.2 - Atelier d'approfondissement de la programmation
<!-- .element style="font-size:0.7em;margin:4em 0;" -->

# Workshop GIT

![](images/common/logo_heg.png)
<!-- .element style="position:absolute; top:0; left:0;width:40%;" class="nopdf" -->

![](images/common/logo_hes-so.jpg)
<!-- .element style="position:absolute; top:0; right:0;width:10%;" class="nopdf" -->

[Boris.Fritscher@he-arc.ch](mailto:Boris.Fritscher@he-arc.ch)
<!-- .element style="position:absolute; bottom:20px; left:0;" class="nopdf" -->

#### Part 4: Advanced Git Commands




# How Git Works

[The Git Parable](https://docs.google.com/presentation/d/1n1b-BSM9w8M48sVdDwaPSqbcy7aQJp2lPYaEMvE6FVw/edit?usp=sharing)

* `git hash-object`
* `git cat-file -t`
* `git cat-file -p`




### Advanced

* **`git reflog`** list all recent actions commit, branch, tag, etc.
* **`git bisect [start|bad|good]`** binary search to find the commit that introduced a bug
* **`git cherry-pick [SHA]`** Apply the changes introduced by some existing commits
* **`git rebase -i`** Reapply commits on top of another base tip (rewrite history)




### How can I?

https://ohshitgit.com/

* delete branch
* delete remote tags, branches
* move branch?
* reset to change branch?
* Reset and move branch name
* rebase vs merge
* Rebase interactive, squash, rewrite history
* Cherry pick




### Out of Scope

* ssh keys
* git aliases
* git hooks, husky
* git submodules/subtree
