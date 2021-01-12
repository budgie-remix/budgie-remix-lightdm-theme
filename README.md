budgie-artwork
==============

Artwork for Ubuntu Budgie

Contains all the artwork for Ubuntu including LightDM and its Greeter

Also the icon-theme for Ubuntu Budgie - Pocillo - is defined

---

# Tela icons

To refresh the tela icons in our project git fork:

    cd ~/Downloads
    git clone https://github.com/ubuntubudgie/tela-icon-theme
    cd tela-icon-theme
    git remote add upstream https://github.com/vinceliuice/tela-icon-theme
    git fetch upstream
    git merge upstream/master
    git commit -m "Latest tela icons"
    git push

Now navigate to tela-icon-theme in this budgie-artwork git project i.e.

    cd tela-icon-theme
    rm -rf *

copy from the tela-icon-theme project its contents into this folder

    cp ../../tela-icon-theme/* .

merge Qogir icons and save

    ./merge.sh
    git add -A
    git commit -m "Merge latest tela/qogir icons"
    git push

---

Use the following to initialise and pull the linked git repos

    git submodule update --init --recursive
