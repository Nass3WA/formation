# Terminal, git et composer

## Commandes terminal basiques

* clear : "efface" le contenu du terminal (en fait ça vous met tout en-dessous)
* pwd : Indique où vous vous situez dans l'arborescence des dossiers
* cd : Permet de se déplacer dans l'arborescence des dossiers
  Exemples :
  cd nomDuDossier/nomDuSousDossier -> nous déplace dans le répertoire nomDuDossier/nomDuSousDossier
  cd -> nous déplace dans le dossier courant (/home/nomUtilisateur)
  cd + double tabulation -> propose une liste de nom de dossiers
  cd debutDuNomDuDossier + tabulation -> autocomplétion du nom du dossier s'il est unique ou sinon liste de dossiers (double tabulation)
  cd .. -> revenir à un niveau d'arborescence au-dessus (ex: revenir au à /sites quand on est sur /sites/dev)
  cd - -> me repositionne là où je m'étais précédemment arrêté dans l'arborescence
* ls : Afficher la liste des dossiers et des fichiers
  Exemples :
  ls -> affiche la liste des dossiers et fichiers du dossier dans lequel on se trouve
  ls /sites -> affiche la liste des dossiers et fichiers du dossier /sites
  ls -l -> affiche une liste plus détaillée du dossier
  ls -a -> affiche la liste des dossiers et fichiers du dossier dans lequel on se trouve (inclus les fichiers cachés)
  ls -al -> combinaison des deux précédentes commandes
* cat : Affiche le contenu d'un fichier

## Git

### Commandes de base

* git init : initialise un dépôt git
* git status : affiche l'état de suivi des fichiers et dossiers
* git add -A : ajout de tous les fichiers au suivi git
* git commit -m "texte de votre commit" : création d'un commit avec le message spécifié
* git config --global user.name "Votre nom" : ajout du nom à la config de git (permet de savoir qui envoie le commit)
* git config --global user.email "Votre email" : ajout du mail à la config de git (permet de savoir qui envoie le commit)
* git log : affiche les derniers commit
* git branch : affiche toutes les branches de votre dépôt
* git remote add origin https://url-du-depot.git : Lien entre votre dépôt local et le serveur remote
* git checkout -b {nom de la branche à créer} : Créer une nouvelle branche
* git checkout {nom de la branche} : Se déplacer vers la branche spécifiée

### Procédure envoi d'un commit vers le serveur remote (par exemple github)

* git add -A
* git commit -m "texte du commit"
* git push -u origin {nomDeLaBranche} (main par défaut sur github)

### Récupérer un projet git

* Se positionner dans le bon dossier
* git clone {url du projet git}

### Récupérer les modifications effectuées sur un projet git

* git pull origin {nomDeLaBranche} (main par défaut)

### Vocabulaire

* Un commit : un enregistrement local (rien n'est envoyé vers le serveur remote)
* Un push : Pousser les modifications faites au dépôt (dans les commit) vers le serveur remote
* Serveur remote : Le serveur git distant vers lequel vous allez enregistrer les changements dans votre code
* Branche : Permet de paralléliser les développements

### Remarques

* cat .git/config : Afficher les informations du fichier de configuration

## Composer

Outil qui permet de gérer toutes les dépendances de votre application (les bibliothèques, les chargements de classes ou de fichiers...).

### Commandes de base

* composer init : Création d'un projet composer dans votre dossier (avec un fichier composer.json)
* composer require {nom de la bibliothèque} : télécharge la bibliothèque dans le dossier vendor
* composer dumpautoload : Met à jour l'autoload de composer à partir de la configuration dans le fichier composer.json

### Liens utiles

* [Doc de composer](https://getcomposer.org/doc/)
* [Liste des packages de composer](https://packagist.org/)