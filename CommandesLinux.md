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
```
