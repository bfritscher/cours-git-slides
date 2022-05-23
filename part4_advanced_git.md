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

#### *Introduction*



git parabol


git hash

eric:hashes_example eric$ git hash-object file1.txt
44bf09d0a2c36585aed1c34ba2e5d958a9379718

eric:hashes_example eric$ git hash-object file2.txt
63ae94dae6067d9683cc3a9cea87f8fb388c0e80

eric:hashes_example eric$ git hash-object file3.txt
782d09e3fbfd8cf1b5c13f3eb9621362f9089ed5

eric:hashes_example eric$ git hash-object file4.txt
a627820d67e455a4f0dfa49c912fbddb88fca483


eric:hashes_example eric$ echo Erik > file5.txt

eric:hashes_example eric$ git hash-object file5.txt
63ae94dae6067d9683cc3a9cea87f8fb388c0e80



Advanced
Rebase vs merge


* **`git reflog`** list all recent actions commit, branch, tag, etc.
* **`git bisect [start|bad|good]`** binary search to find the commit that introduced a bug
* **`git cherry-pick [SHA]`** Apply the changes introduced by some existing commits
* **`git rebase -i`** Reapply commits on top of another base tip (rewrite history)


git rebase squash
delete remote tags, branches


delete branch?
move branch?
reset to change branch?
Manipuler l’historique
Rebase interactive
Cherry pick
Reset and move branch name



### Out of Scope
ssh keys
git aliases
git hooks, husky
git submodules/subtree
https://ohmygit.org/
https://ohshitgit.com/
