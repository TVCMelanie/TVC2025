# Rappel des commandes Linux
## Lister le contenu d'un répertoire
### Les bases
- Trouver le terminal : Ctrl + Alt + t
- bash
---
- Hirarchie stanrd de Linux : 
- / (racine) : Contient tous les fichiers et répertoires du système.

 - */bin & /sbin* : Programmes et commandes essentielles pour tous les utilisateurs (bin) et pour l'ad
ministration (sbin).
 - */etc* : Fichiers de configuration du système et des services.
- */home* : Dossiers personnels des utilisateurs (ex. /home/stagiaire).
- */var* : Données variables comme logs (/var/log) et files d’attente (/var/spool).
- */usr* : Logiciels et bibliothèques utilisateur (/usr/bin, /usr/lib).
- */opt* : Applications tierces installées manuellement.
- */tmp* : Fichiers temporaires supprimés au redémarrage.
- */dev, /proc, /sys* : Systèmes de fichiers spéciaux pour les périphériques et processus.
- */boot* : Contient les fichiers nécessaires au démarrage, comme le noyau Linux (vmlinuz), le chargeur
 de démarrage (GRUB).
- */media* : Points de montage pour les périphériques amovibles (clés USB, disques durs externes,
 CD/DVD).
- */mnt* : Point de montage temporaire pour des systèmes de fichiers externes.
- */root* : Dossier personnel de l'utilisateur root (administrateur).
- */run* : Stocke les informations volatiles du système (PID, sockets, fichiers de verrouillage) après le
 démarrage.
- */srv* : Contient les données des services hébergés par le système (serveurs web, FTP, etc.)

---
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

## Les options de la commande LS
-Ajouter la récursive (affiche dans l'odre inverse)
```bash
ls -rl
ls -lr
ls -l -r
```

-Affiche le répertoire de /var/log
```bash
ls -l /var/log/
```

-Affiche le répertoire de /var/log par ordre d'horodatage
```bash
ls -lt /var/log/
```

-Affiche le répertoire de /var/log selon la taille du ficher
```bash
ls -l -s /var/log/
```

-Affiche le répertoire de /var/log mais inverse tout type de tri :
```bash
ls -lsr /var/log/
```

-Affiche le répertoire de /var/log
```bash
ls -l /var/log/
```



