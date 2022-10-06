### GIT Associative/notes
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
* git log -p            / näitab konkreetsed muudatused

## Git status
¤ Failid saavad olla jälgitavas ja mitte jälgitavas olekus
* git status            / näitab projekti olekut

## Git add
¤ Vaja lisada failid enne commiti stg
* git add <file>        / lisab faili stg
* git add <directory>   / lisab terve repo
* git add -p            / vali käsitsi mida lisada. (y, n, s, e, q)
* git add .             / lisab kõik

¤ Kui on vaja teha erinevatele failidele erinevad commit
¤ git add <file1> <file2>  ja commit need jne

## Git commit
* git commit                    / salvestab jooksva muudatuse
* git commit -m "change text"   / salvestab muudatuse ja lisab kohe kommentaari

## Git restore
* git restore <file>    / viib faili eelmise commit olekusse

## Git diff
* git diff              / näitab viimaseid muudatusi eelmisest commit
