=========================
Cartolacôte documentation
=========================

Prérequis
---------

* Installer le Windows Terminal (depuis Microsoft Store)

Activer la virtualisation sur Windows : 

* Ouvrir le terminal 
* Executer les deux lignes de commandes ci-dessous (conseil : effectuer le redemarrage après la deuxième commande): 

:: 

  Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
  Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

* Ouvrir le Windows Terminal 
* Executer la commande suivante : ``wsl.exe --set-default-version 2``
* Installer Ubuntu (dernière LTS, depuis Microsoft)
* Depuis le menu windows, lancer Ubuntu
* Indiquer un nom d'utilisateur et un mot de passe 
* Fermer le terminal et la fenêtre linux 
* Relancer le terminal
* Verifier que la console linux apparaît dans la liste des consoles 

  * Si ce n'est pas le cas, ajouter la console dans le ficher suivant ``%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\``
  
:: 

            {
                "guid": "{2c4de342-38b7-51cf-b940-2309a097f518}",
                "hidden": false,
                "name": "Ubuntu",
                "source": "Windows.Terminal.Wsl",
                "startingDirectory": "C:\\Users\\fanguin.p"
            },


Effectuer les mise à jour et installer les dépendances linux : 
:: 

  sudo apt-get update
  sudo apt-get install python3-sphinx
  sudo apt install make
  sudo apt install python3-pip
  pip3 install PyStemmer

Installation
------------

Le projet github comporte deux branches : 

* ``master`` : contient les fichiers rst et la configuration python
* ``gh-pages`` : contient les fichiers html générés par la compilation

La structure des dossiers dans les deux branches n'est pas la même c'est pour cela qu'il est nécessaire d'avoir deux dossiers séparés :

* cartolacote-documentation : les modifications sont faites dans la branche ``master``
* cartolacote-docs-build : les modifications sont faites dans la branche ``gh-pages``

::

  git clone https://github.com/sitnyon/cartolacote-documentation.git cartolacote-documentation
  mkdir cartolacote-docs-build
  cd cartolacote-docs-build
  git clone https://github.com/sitnyon/cartolacote-documentation.git html
  cd html
  rm -rf docs
  rm README.rst
  git checkout gh-pages-private

Les deux dossiers sont mis en place. 

Compiler les fichiers html
--------------------------

Les modifications des fichiers ``rst`` doivent être faites dans le dossier ``cartolacote-documentation``

:: 

  cd  cartolacote-documentation/docs/
  make html

Pour tester les modifications aller sous : ``cartolacote-docs-build/html/`` et ouvrir le fichier index.html

Commiter les changements
------------------------

Dans la branche ``master`` : 

:: 

  cd cartolacote-documentation/
  git add -u # Fait un git rm pour tous les fichiers supprimés
  git add .
  git commit -m 'Add changes to the doc'
  git push origin master

Dans la branche ``gh-pages`` :

:: 

  cd cartolacote-docs-build/html/
  git add -u # Fait un git rm pour tous les fichiers supprimés
  git add .
  git commit -m 'Rebuilt files'
  git push origin gh-pages


