!SLIDE commandline
# Opzetten

    $ cd mijn/werkmap
    $ git init lijstje
    $ git init
    Initialized empty Git repository in /tmp/...
    $ cd lijstje/
    $ git status
    On branch master
    Initial commit

!SLIDE commandline
# Config

    $ git config --global user.email "ber@berk.es"
    $ git config --global user.name "Bèr Kessels"

!SLIDE commandline
# Index (staging)
    $ edit supermarkt.txt
    $ git add supermarkt.txt
    $ git status

!SLIDE commandline
# Committing
    $ git commit
    $ git status

!SLIDE commandline
# Nog een keer
    $ edit supermarkt.txt # Voeg "Melk<enter>Suiker" aan toe
    $ cat supermarkt.txt
      Boodschappenlijstje

      Melk
      Suiker
    $ git add supermarkt.txt
    $ git commit supermarkt.txt # Suiker en melk toegevoegd

!SLIDE commandline
# Bekijken
    $ git status
    On branch master
    nothing to commit, working directory clean

    $ git log

    $ git diff <eerste sha> HEAD

    $ git show <sha>

!SLIDE commandline
# Teruggaan
    $ git log --oneline --decorate
    $ git checkout <eerste sha>
    NOTE!
    $ git log --oneline --decorate
    $ git checkout master # of <laatste sha>
    $ git log --oneline --decorate

!SLIDE commandline
# Terugdraaien
    $ # Voeg "Eieren" toe, stage en commit
    $ git revert HEAD

    $ git log

!SLIDE commandline
# Geheel verwijderen
    $  git reset --hard <sha melk en eieren>
