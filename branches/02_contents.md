!SLIDE commandline
$ edit "markt.txt"

!SLIDE bullets incremental
# Vijf voor negen.
* Printen, naar supermarkt.

!SLIDE commandline
$ git status
$ git checkout?
$ git revert?
$ git reset?

!SLIDE commandline
# Branches
$ git branch markt
$ git checkout markt
$ git status
$ git add en commit
$ git log --oneline --decorate

# Master en Markt
$ git checkout master
$ edit supermarkt.txt # Add Yoghurt
$ git add en commit
$ git log --oneline --decorate
  Merk op dat de commit in Markt mist!

# Reviewen
$ git log --oneline --decorate --graph --all

!SLIDE code

    * 5fd65b3 (HEAD, master) add yoghurt
    | * 2183c5b (markt) Moved Eieren to markt.txt
    |/  
    * 0039e29 Add Melk en Suiker
    * 552f69e Adding initial supermarket

!SLIDE bullets incremental
# Panic averted. We kunnen toetje eten, straks

!SLIDE commandline
$ git checkout master
$ git merge markt
$ git status
$ git log --oneline --decorate --graph --all
$ git branch -d markt

!SLIDE commandline
# Mergeconflicten
$ git branch koppen
$ git checkout koppen
$ edit supermarkt.txt # wijzig kop in "Kopen in Supermarkt"
$ git add en commit

!SLIDE commandline
$ git checkout master
$ edit supermarkt.txt # wijzig kop in "Kopen in Jumbo"
$ git add en commit

!SLIDE commandline
$ git checkout master
$ git merge koppen
  Mergeconflict in supermarkt.txt
$ git status
$ edit supermarkt.txt

!SLIDE code

    <<<<<<< HEAD
    Kopen in Jumbo
    =======
    Kopen in Supermarkt
    >>>>>>> koppen

    Melk
    Suiker
    Yoghurt

!SLIDE commandline
# Mergeconflict oplossen
$ edit supermarkt.txt
$ git add supermarkt.txt
$ git commit
