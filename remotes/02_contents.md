!SLIDE commandline

    $ cd ../
    $ git clone lijstje nieuwlijstje
    $ cd nieuwlijstje
    $ git log
    $ git branch -v
    $ git remote -v

!SLIDE code small

    origin	/tmp/guest-kk71Nw/Documents/lijstje (fetch)
    origin	/tmp/guest-kk71Nw/Documents/lijstje (push)

!SLIDE commandline

    $ cd ../lijstje
    $ git remote -v

!SLIDE commandline
    $ edit supermarkt.txt
    $ git commit en add in master

    # Protip:
    $ echo "Kaas" >> supermarkt.txt && git commit -am "Kaas toegevoegd"
    # Don't try this at home!

!SLIDE commandline
# Pull
    $ cd ../nieuwlijstje
    $ git status
    $ git log
    $ git pull origin master
    $ git log --oneline --decorate --graph

!SLIDE commandline
# Push
    $ cd ..
    $ git clone --bare lijstje backuplijstje
    $ ls -ahl backuplijstje
    $ ls -ahl lijstje/.git

!SLIDE commandline
    $ cd lijstje
    $ git remote add origin /.../backuplijstje/
    $ git remote -v

!SLIDE commandline
    # Voeg "kaas" to, add en commit.
    $ git push origin master
