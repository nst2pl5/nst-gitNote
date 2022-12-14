### GIT Associative
¤ https://www.atlassian.com/ru/git
¤ GIT Sheme: repo -> stg -> commit.
¤ Git commit arvutab kogu projekti hash summa ja alles siis kui vastav hash erineb eelmisest salvestab selle

## Git SHH connect
* ssh-keygen -o -t rsa -C "nikita.stsigorjev@gmail.com"             / to terminal, add ssh to C:\Users\Kasutaja\.ssh
¤ copy public key and paste to git settings->SSH and GPG keys
* git clone <git-repo-SHH>                                          / laeb giti serverist alla seal oleva repo

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

## Git reset
* git reset --hard                      / võtab kõik muudatused tagasi
* git reset --hard <commit-hash>        / võtab kõik muudatused tagasi ja viib HEAD kindla commiti olekusse
* git reset --mixed                     / võtab tagasi viimase stg lisatud faili

## Git branch
* git branch -a                 / näitab kõiki repos olevaid branche
* git branch <branch-name>      / loob uue branchi
* git branch -d <branch-name>   / kustutab valitud branch (kui kasutada -D siis kustutab igalt poolt)

## Git checkout
* git checkout <branch-name>                    / viib repo üle nimetatud branchile
* git checkout <commit-hash>                    / viib repo üle nimetatud commitile
* git checkout -b <branch-name>                 / teeb uue branch ja kohe viib HEAD sellele
* git checkout -b <branch-name> <commit-hash>   / teeb uue branch, viib selle commiti olekusse ja kohe viib HEAD sellele
* git checkout <file-name>                      / viib kindla faili algsesse olekusse

## Git merge
* git merge <branch-name>       / sulatab käesoleva branchi muudatused valitud branchiga

## Git remote
¤ manipuleerib kaug serveriga
* git remote add <name> <repo-SSH>              / uue ühenduse loomine (lisab fetch ja push repo)
* git remote rm <name>                          / kustutab ühenduse
* git remote rename <old-name> <new-name>       / nimetab ühenduse ümber
* git remote -v                                 / näitab kõiki ühendusi

## Git push
* git push                                              / lisab commit serverisse
* git push <name-to> <branch-name-to>                   / saadab andmed nimetatud kohta
* git push --set-upstream <name-to> <branch-name-to>    / peale seda võib lihtsalt: git push ja git pull

## Git pull
* git pull                                          / tõmbab viimase uuenduse serverist
* git pull <name-from> <branch-name-from>           / tõmbab andmed nimetatud kohast

## Git fetch
* git fetch                                     / uuendab repo kõige uuemaks

## Git rebase
* git rebase master                             / ühendab 2 haru commit omavahel

## Git tag
* git tag -a <tag-name> -m "<tag-commit>"       / lisab tagi jooksvale commitile
* git push --tags                               / lisab kõik tagid srverisse