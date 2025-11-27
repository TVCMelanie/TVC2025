# Rappel des commandes Linux
## Lister le contenu d'un répertoire
- Trouver le terminal : Ctrl + Alt + t
- bash
```bash
```
- Hirarchie stanrd de Linux : 
```bash
ls -l / : Lister le contenu à partir de la racine
/ : racine, contient tous les fichiers et répertoires du système
/bin & /sbin :
/etc :
/home :
/var :
/usr :
/opt :
/tmp :
/dev, /proc, /sys :
/boot :
/media :
/mnt :
/root : 
/run :
/srv :
```
- Lister le contenu à partir de la racine
```bash
ls -l /
```

- Nettoyer son écran de terminal
```bash
clear
```

- Trouver le manuel d'aide
```bash
man ls
man echo
```

- Savoir où je suis placé
```bash
pwd
```
-Aller puis Quitter un répetoire 
```bash
cd Téléchargements
cd ~ : Retourner dossier personnel
cd .. : remonte d'un niveau
cd/home/stagiaire : retour par la racine
cd ../Documents/
cd ~ /documents/ : Se déplacer entre dossier 
```

- changer de dossier
```bash
cd
cd Documents/
cd /Hom
```

- Indiquer le dossier courant (où on se trouve)
```bash
pwd
```

- Créer un dossier
```bash
mkdir ~/dossier_Test
```
- Supprimer un fichier ou un dossier
```bash
rm text.txt
rm -R ~/dossier_Test
```
- Copier un fichier ou un dossier
```bash
cp -R ~/Téléchargements ~/Téléchargements2
```
Pas besoin de ~ si on est dans le répertoire, si on ne l'est pas ~ obligatoire

- Trouver un fichier
```bash
find -name toto.txt
find name passwd
```

-Copier un ficher dans un autre dossier
```bash
cp -R Documents/ Téléchargements/
(document c'est la source vers la destination)
```

-déplacer un ficher dans un autre dossier
```bash
mv /home/stagiaire/fichier1.txt /Documents/
```

-Copier un ficher dans un nouveau dossier à créer
```bash
mkdir ~/nouveauDoss/ && cp toto.txt ~/nouveauDoss/
```
-Récursivité, va regarder l'ensemble des dossiers et sous dossier et tout prtendre en compte
```bash
-R
```

-entireté du contenu du dossier
```bash
*
```

-Créer un fichier ou créer un fichier vers une direction précisise
```bash
touch fichier1.txt
touch /home/stagiaire/fichier1.txt
```

-Affiche le contenu du ficher
```bash
cat fichier1.txt
```

-Ouvrir en console dans un éditeur
```bash
nano fichier1.txt
``` 

-Supprimer le contenu d'un ficher texte
```bash
echo "Coucou" > fichier1.txt
```

-Ajouter du texte à un fichier texte
```bash
echo "coucou" >> fichier1.txt
```
