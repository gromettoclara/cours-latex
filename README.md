## PAO – LaTeX

Introduction à LaTeX 

M1 Master HN Université de Rouen

S2 / 15 heures de TD

## [Lien vers les slides](https://gromettoclara.github.io/cours-latex/cours.slides.html#/)

## Pratiquer

Pour écrire et compiler du LaTeX, vous avez besoin : 

- d'un éditeur de texte
- d'ouvrir un terminal pour lancer la commande
- avoir la distribution LaTeX installée sur votre machine

### Installer LaTeX

Attention, la TeXLive est très lourde et assez longue à installer. 

#### Windows 

Téléchargez l'installeur : [https://tug.org/texlive/](https://tug.org/texlive/), téléchargez le `.exe` et exécutez-le. Une fenêtre s’ouvre (installateur TeX Live). Cliquez sur `Advanced`pour pouvoir configurer l’installation. Il faut choisir un profil d'installation. 
- full → tout installer (recommandé si vous avez la place)
- medium → bon compromis

#### MacOS

Installer MacTeX qui inclut la TeX Live et un éditeur simple (TeXShop). Téléchargez l'installeur depuis : https://tug.org/mactex/ et lancez le fichier `.pkg`. 

#### Linux 

**Attention**: ne **PAS** installer LaTeX depuis les dépots linux (selon la méthode habituelle d'installation des paquets). Si vous avez déjà installé latex par le biais de `apt install`, il faut au préalable le désinstaller.

Avoir le package `perltk` installé. Si ce n'est pas le cas:
- Ouvrez un terminal
- Tapez la commande suivante: `sudo apt install perl-tk` et validez par la touche "Retour"
- Tapez votre mot de passe (il reste invisible, c'est normal), et validez par la touche "Retour"

Puis **téléchargez le package d'installation**. Deux possibilités : 

1. Téléchargez le fichier *via* le lien suivant: [install-tl-unx.tar.gz](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz)
2. Dans le terminal, placez-vous dans le dossier Téléchargement par la commande `cd ~/Téléchargements` puis tapez `wget https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz`

Une fois le fichier téléchargé, décompressez-le. Pour cela, double-cliquez dessus ou tapez dans le terminal la commande `tar -xf install-tl-unx.tar.gz`

**Installation :**

1. Dans le terminal, placez-vous dans le dossier que vous avez décompressé par la commande `cd` suivie du nom du dossier (`install-tl-20251016`; le nombre peut être différent). Vous pouvez utiliser la touche Tab pour activer l'autocomplétion du nom du dossier.
2. Tapez `sudo perl install-tl`
3. Si vous avez de la place sur votre ordinateur et une bonne connexion internet: répondez `i` ("start installation to hard disk"). **Cette option est à privilégier**
4. Si votre connexion est mauvaise, ou que vous avez trop peu de place, vous pouvez au choix:
	- tapez`c` pour sélectionner quelques collections de packages à décocher. Vous pouvez enlever sans problème les collections désignées par les lettres suivantes: `iklmnowxyzABCPS`. Attention, certaines collections seront utiles si vous comptez utiliser les langues concernées (par exemple arabe ou persan dans la collection `arabit`. Dans ce cas, ne les indiquez pas).
	- Si même ainsi cela prend trop de place/de temps, tapez `j` pour sélectionner un schéma et choisissez "teTex"   

	-> Tapez ensuite `r` pour retourner au menu principal, et `i` pour lancer l'installation.  
Il sera de toute façon possible d'installer plus tard ces collections si vous en avez besoin. 

**Config :**

Il ne reste plus qu'à configurer votre installation:

1. Tapez dans le terminal  `sudo nano  ~/.profile`. Vous devrez ensuite taper votre mot de passe (qui reste invisible, c'est normal!). Si vous n'avez pas nano, vous pouvez l'installer, ou ouvrir le fichier avec un autre logiciel, par exemple avec gnome-text-editor: `sudo gnome-text-editor  ~/.profile`
2. Dans le fichier qui s'ouvre, ajoutez les lignes suivantes: 

```
PATH=/usr/local/texlive/2025/bin/x86_64-linux:$PATH; export PATH
MANPATH=/usr/local/texlive/2025/texmf/doc/man:$MANPATH; export MANPATH
INFOPATH=/usr/local/texlive/2025/texmf/doc/info:$INFOPATH; export INFOPATH
```

3. Enregistrez le fichier, puis tapez dans le terminal `source ~/.profile` pour que le changement soit pris en compte.
4. Vérifiez que tout fonctionne en tapant `which xelatex` dans le terminal: vous devez avoir le chemin de la texlive 2025 qui s'affiche.

## LaTeX made easy ?

- Overleaf vous laisse encore compiler environ 20 fois par mois... 
- [Papeeria](https://www.papeeria.com/) vous permet d'éditer gratuitement un projet à la fois
- Un serveur Overleaf auto-hébergé est accessible pendant les séances de cours. Attention, les données ne seront pas sauvegardées et pourront être effacées. L’URL d’accès est : http://overleaf-lsh.univ-rouen.fr. **Cette URL n’est accessible que depuis les salles de cours du bâtiment informatique 6B de l’UFR**. Pour tester cette solution, il est nécessaire de créer des comptes utilisateurs en indiquant vos adresses mail universitaires. Une fois enregistrés, vous recevrez un message sur vos boîte universitaire vous invitant à vous connecter au serveur Overleaf-LSH et à choisir un mot de passe
- Les postes de la salle 204 sont équipés de LaTeX et de TeXStudio

## Évaluation 

1H30 lors du dernier cours

- 50% questions de cours
- 50% exercices

Le cours, la prof et google à disposition. 
