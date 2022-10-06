### GIT Associative/notes
¤ https://www.atlassian.com/ru/git
¤ GIT Sheme: repo -> stg -> commit.
¤ Git commit arvutab kogu projekti hash summa ja alles siis kui vastav hash erineb eelmisest salvestab selle

## Git config
¤ Konfigureerib andmeid
* git config --system   / kõik kasutajad
* git config --global   / konkreetne kasutaja
* git config --local    / lokaalne repo
* git config --list     / näitab kõik andmed

## Git init
* git init              / initsialiseerib git projekti antud repos

## Git log
* git log               / näitab muutuste logi projektis
* git log --oneline     / näitab vastuseid 1 rea peal
* git log -p            / näitab konkreetsed muudatused

## Git show
* git show <commitNr>   / näitab commitis tehtud muudatusi

## Git status
¤ Failid saavad olla jälgitavas ja mitte jälgitavas olekus
* git status            / näitab projekti olekut

## Git add
¤ Vaja lisada failid enne commiti stg
¤ kui peale stg lisamist on tehtud veel muudatusi siis on vaja see fail uuesti lisada stg
* git add <file>        / lisab faili stg
* git add <directory>   / lisab terve repo
* git add -p            / vali käsitsi mida lisada. (y, n, s, e, q)
* git add .             / lisab kõik

¤ Kui on vaja teha erinevatele failidele erinevad commit
¤ git add <file1> <file2>  ja commit need jne

## Git commit
* git commit                                            / salvestab jooksva muudatuse
* git commit -m "change text"                           / salvestab muudatuse ja lisab kohe kommentaari
* git commit -a -m "change text"                        / salvestab muudatuse, lisab stg ja kohe kommentaari
* git commit --amend                                    / lisab muudatuse HEAD commiti
* git commit --amend -m "change last commit text"       / lisab muudatuse HEAD commiti ja muudab commiti texti

## Git restore
* git restore <file>    / viib faili eelmise commit olekusse
* git restore .         / viib kogu failide puu eelmise commiti olekusse

## Git diff
* git diff              / näitab viimaseid muudatusi eelmisest commitist
* git diff --staged     / näitab muudatusi mis on juba indekseeritud

## Git mv
¤ saab muuta faili nime ja liigutada folderite vahel
¤ samuti mv rakendab kohe git add mõjutatavale failile
* git mv <file-name> <new-name> || git mv <file> </to-directory>

## Git rm
¤ saab kustutada
¤ rakendub kohe ja pole vaja git add to stg
* git rm <file> || git rm <directory>

## Git .gitignore
¤ saab rakendada reeglid mida git ignoreerib
* loo fail .gitignore

================================================================================
Git branches tree

## Git branch
* git branch -a                 / näitab kõiki repos olevaid branche
* git branch <branch-name>      / loob uue branchi
* git branch -d <branch-name>   / kustutab valitud branch (kui kasutada -D siis kustutab igalt poolt)

## Git checkout
* git checkout <branch-name>    / viib repo üle uuele branchile

## Git bugfixmerge
* git merge <branch-name>       / sulatab käesoleva branchi muudatused valitud branchiga