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

#### Part 0: Requirements

#### *Terminal and Software*




### Command line commands

![](images/xkcd-tar.png)

<!-- .element: class="center" -->

- What commands do you know ?
- What do they do ?
- How to exit a running command line program ?



Command | Description
--- | ---
`d:` | Change the drive
`cd` | Change directory
`ls` | List files
`cat` | Display a file's content
`mkdir` | Create a directory
`ni` | Create a new file
`echo "hello" > ` *file* | Write a string to a file
`echo "hello" >> ` *file* | Append a string to a file
`rm` | Remove a file
`mv` | Move a file
`cp` | Copy a file
`start` | Start a program (Windows)
`pwd` | Print working directory
`clear` | Clear the screen

[PowerShell](https://apps.microsoft.com/store/detail/powershell/9MZ1SNWT0N5D?hl=fr-ch&gl=CH)

<!-- .element: class="smallerr" -->




### Chemins absolus et relatifs
- le point (.)  répertoire courant
- deux pointillés (..)  répertoire parent.

![](images/arcgis-folders.gif)<!-- .element: class="w-25 float-left" -->


 D:\Data\Shapefiles\Landuse comme répertoire courant :
 <!-- .element: class="small" -->

```sh
..               (D:\Data\Shapefiles)
..\..            (D:\Data)
..\..\Final      (D:\Data\Final)
.                (D:\Data\Shapefiles\Landuse - the current directory)
.\..\Soils       (D:\Data\Final\Soils)
..\..\.\Final\..\Shapefiles\.\Landuse  (D:\Data\Shapefiles\Landuse)
```
<!-- .element: class="w-70 float-right" -->

https://desktop.arcgis.com/fr/arcmap/10.3/tools/supplement/pathnames-explained-absolute-relative-unc-and-url.htm

<!-- .element: class="credits" -->

[demo_folders.zip](/files/demo_folders.zip)

<!-- .element: class="credits" -->




<!-- .slide: data-background-video="images/windows-terminal.mp4" data-background-video-muted data-background-video-loop -->
### [Windows Terminal](https://www.microsoft.com/fr-ch/p/windows-terminal/9n0dx20hk701?rtc=1&activetab=pivot:overviewtab)




### Exercice: Commande Line

Quels sont les lignes de commandes à effectuer pour obtenir le résultats demandés ?:

[Quiz](https://forms.office.com/Pages/ResponsePage.aspx?id=fX07WxnhBU2QIvd18uSOlnwGT4lx77ZFo6AQM_5Ntr9UMUpPSUdUUk0zRkJCRTlWSlBJMTVNTDBCWi4u)

- Télécharger le fichier [exercice_commande_line.tar.gz](/files/exercice_commande_line.tar.gz)
- Extraire le fichier
- Consulter le fichier `Readme.md` et suivre les instructions


