<style>
    li {
        transition: all 0.5s;
    }
    li:hover {
        font-size: 120% !important;
        margin: 0.5em 0 !important;
        cursor: pointer !important;
    }
</style>
63-21.2 - Atelier d'approfondissement de la programmation
<!-- .element style="font-size:0.7em;margin:4em 0;" -->

# Workshop GIT

![](images/common/logo_heg.png)
<!-- .element style="position:absolute; top:0; left:0;width:40%;" class="nopdf" -->

![](images/common/logo_hes-so.jpg)
<!-- .element style="position:absolute; top:0; right:0;width:10%;" class="nopdf" -->

[Boris.Fritscher@he-arc.ch](mailto:Boris.Fritscher@he-arc.ch)
<!-- .element style="position:absolute; bottom:20px; left:0;" class="nopdf" -->

#### Part 2: Git Collaborate with others and GitHub Workflow




# GitHub

[GitHub](https://github.com/) is a web-based Git repository hosting service, adding
its own features:

Wikis, bug tracking, **Markdown** rendering and static page hosting.

Unlike Git, which is strictly a command-line tool, GitHub provides
a web-based **graphical interface**



### Github Web

Browse commits, issues, fork, pull requests, wiki, Readme.md

![](images/github-project.jpg)




### Distributed VCS like Git

![](images/vcs-distributed.png)<!-- .element: class="w-50" -->

<!-- .element: class="center" -->



### GIT remote

* **`git remote add [alias] [url]`** add a git URL as an alias
* **`git fetch [alias]`** fetch down all the branches from that Git remote
* **`git merge [alias]/[branch]`** merge a remote branch into your current branch to bring it up to date
* **`git push [alias] [branch]`** Transmit local branch commits to the remote repository branch
* **`git pull`** fetch and merge any commits from the tracking remote branch
* **`git clone [uri]`** retrieve an entire repository from a hosted location via URL

<!-- .element: class="small" -->



### Exercice: GitHub Remote

1. Créer un compte [GitHub](https://github.com/signup)
2. Créer un repository sur GitHub [Classroom git](https://classroom.github.com/a/hviP49Kz)
3. Créer un repository git local (avec au moins 1 commit) et connectez-le à GitHub
4. Ajouter des commit local et envoyé les sur le remote
5. Cloner le repository remote dans un autre dossier
6. Ajouter un nouveau commit, envoyé le sur le remote, et récupéré le dans le premier dossier local

<!-- .element: class="small" -->




# Markdown
## From text to HTML



### Markdown Basics

[Markdown](http://daringfireball.net/projects/markdown/syntax) allows you to write using an easy-to-**read**, easy-to-**write** plain **text format**, which then converts to valid HTML.

```markdown
# The largest heading (an <h1> tag)
## The second largest heading (an <h2> tag)

> Blockquotes

Text styling *italic* and **bold**

Links (<a href="url">title</a>)
[title](url)

Images (<img src="src" alt="">)
![alt](src)
```



### Markdown List and Table

```markdown
Unordered lists
* Item
* Item

- Item
- Item

Ordered lists
1. Item 1
2. Item 2
3. Item 3

some: `c0de`

| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |
```
<!-- .element: class="float-left w-50" -->

* Item
* Item

<br/>

1. Item 1
2. Item 2

&nbsp;&nbsp;some: `c0de`

| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |



### Visual Studio Code

Can preview markdown in realtime.

<!-- .element: class="smaller" -->

![](images/vscode_markdown_preview.png)

<!-- .element: class="w-60" -->

Warning: markdown on github is a special variant!

<!-- .element: class="red" -->




### Github Flow

![](images/Github-flow.png)



### Github Fork

![](images/github-fork.png)

<!-- .element: class="w-80" -->



### Github Labs

* https://lab.github.com/githubtraining/introduction-to-github

<!-- ( https://lab.github.com/githubtraining/communicating-using-markdown ) -->

* https://lab.github.com/githubtraining/managing-merge-conflicts

* https://lab.github.com/githubtraining/reviewing-pull-requests

* https://profy.dev/project/github-minesweeper/intro-overview


