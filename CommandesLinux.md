use# Rappel des commandes Linux
## Lister le contenu d'un répertoire
## Les bases
- Trouver le terminal : Ctrl + Alt + t
- Retrouver l'invite de commande : Ctrl + c
- Entrainement shell : https://chinginfo.fr
- bash
---
. est le raccourci représentant le répertoire courant
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
- Aller puis Quitter un répetoire 
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

- Copier un ficher dans un autre dossier
```bash
cp -R Documents/ Téléchargements/
(document c'est la source vers la destination)
```

- Déplacer un ficher dans un autre dossier
```bash
mv /home/stagiaire/fichier1.txt /Documents/
```

- Copier un ficher dans un nouveau dossier à créer
```bash
mkdir ~/nouveauDoss/ && cp toto.txt ~/nouveauDoss/
```
- Récursivité, va regarder l'ensemble des dossiers et sous dossier et tout prtendre en compte
```bash
-R
```

- Entireté du contenu du dossier
```bash
*
```

- Créer un fichier ou créer un fichier vers une direction précisise
```bash
touch fichier1.txt
touch /home/stagiaire/fichier1.txt
```

- Affiche le contenu du ficher
```bash
cat fichier1.txt
```

- Ouvrir en console dans un éditeur
```bash
nano fichier1.txt
``` 

- Supprimer le contenu d'un ficher texte et remplace
```bash
echo "Coucou" > fichier1.txt
```

- Ajouter du texte à un fichier texte
```bash
echo "coucou" >> fichier1.txt
```

- Arrêt
Necessite un accès admin
```bash
shutdown [option] heure [message]
shutdown 01.51
shutdown +1 "Goodbuy World"
```
---
## Les options de la commande LS
- Ajouter la récursive (affiche dans l'odre inverse)
```bash
ls -rl
ls -lr
ls -l -r
```

- Affiche le répertoire de /var/log
```bash
ls -l /var/log/
```

- Affiche le répertoire de /var/log par ordre d'horodatage
```bash
ls -lt /var/log/
```

- Affiche le répertoire de /var/log selon la taille du ficher
```bash
ls -l -s /var/log/
```

- Affiche le répertoire de /var/log mais inverse tout type de tri :
```bash
ls -lsr /var/log/
```

- Affiche le répertoire de /var/log
```bash
ls -l /var/log/
```

---
## La commande SU et SUDO
La commande su permet de se mettre en compte super utilisateur
La commande sudo permet de se mettre en compte root pour une commande


- Permet de se connecter en super utilisateur, demande le mdp root
```bash
su -
su -l
sur --login
```

- Quitter le mode super utilisateur
```bash
exit
```

- Basculer vers un autre compte utilisateur avec sudo
```bash
sudo -u
```
---
## Les permissions d'un fichier
-Modifier les autorisation d'un fichier ou d'un répertoire
```bash
chmod
```

- Modifier la propriété d'un fichier, d'un groupe par root
```bash
chown
```
ex : Je veux changer le ficher hello.sh qui est noté en utilisateur pour root
```bash
sudo chown root hello.sh
puis vérifier
ls -l hello.sh
```

- Exécuter le script après avoir mis un ficher propriétaire root
```bash
sudo ./hello.sh
```

---
## Les affichages de ficher
La commande "cat" affiche les 5ière ligne du fichier

- Afficher page par page sur des fichier volumineux
```bash
Afficher lignes du haut
head [option] [fichier]

Afficher ligne du bas
tail [option] [fichier]

head alpha.txt
```

- L'option pour spécifier le nombre de lignes à afficher
```bash
-n
head -n [nombre de lignes] [nom du ficher]
ex : head -n 5 alpha.txt
```

---
## Les Copies et Remove fichiers
Les autorisations peuvent avoir un impact sur les commandes de gestion de fichiers, pour copier un fichier il est nécessaire d'avoir l'autorisation d'éxécution pour accéder au répertoireoù se trouve le fichier et l'autorisation de lecture pour le fichier en cours de copie.
Il aussi avoir l'autorisation d'écriture et d'éxécution sur le répertoire dans lequel le fichier est copié ou déplacer.

- Copier le fichier ou des partitions entières au niveau du bit.
```bash
dd [option] opérand
```

- Déplacer un fichier
```bash
mv people.csv Work
Le ficher à déplacer people.csv vers l'endroit choisi Work
Puis vérifier
ls Work
```

- Déplacer plusieurs fichiers vers 1 lieu choisi
```bash
mv people.csv alpha.txt letter.txt Work
```
---
## Suppression de fichiers
```bash
rm [option] fichier [fichier]
```

Utiliser les récursive *-r* pour supprimer un répertoire, attention, ça supprime tous les fichiers et sous répertoires

---
## Filtrage d'entrée
Filtre qui recherche les entrées et renvoie les lignes qui contiennent une correspondance avec un motif donné.
```bash
grep [option] motif [fichier]
```

- '' : Des guillemets simple peuvent être mis pour être protégé et ainso que le shell ne les interprête pas en caractère spéciaux. Ex : 'root'
- ^ : Permet de s'assurer qu'un motif apparait en début de ligne. Ex : '^root'
- $ : Peu être utliser pour s'assurer qu'un motif apparait à la fin de la ligne. Ex : 'r$'
- * : Utilisé pour faire correspondre zéro ou plusieurs occurences d'un caractère ou d'un motif précédent

```bash
grep 'r..t' red.txt
Trouve les mots du fichier qui commencent par r et finissent par t et le poind remplace un caractère

grep'....' red.txt
Affiche les mots en 4 lettres en rouge et le reste des lettres des mots en plus est rouge

grep '[0-9]' profile.txt
Affiche en rouge les chiffres de 0-9 sur le fichier

grep 're*d' red.txt
Affiche les caractères qui se rapproche
```
---
## Configuration réseau
```bash
iwconfig et ifconfig
Affiche les infos du réseau dont l'ipv4
```

- La commande ping
```bash
ping 192.168.1.2
La commande continuera d'envoyer des paquets jusqu'à interruption Ctrl+c

L'option -c suivi du nombre de pings à envoyer
ping -c 4 192.168.1.2
```

- Affichage des processus
Affiche les processus en cours d'éxécution sur le terminal actuel
```bash
ps [ption]
```

- *PID* : L'identification du processus, qui est unique au processus. Ces informations sont utiles pour controler le processus par son num d'identification
- *TTY* :  Le nom du terminal sur lequel le processus est en cours d'éxécution. Ces informations sont utiles pour distinguer les diff processus qui portent le même nom.
- *TIME* : Le temps processeur utilisé par le processus. Généralement, cette information n'est pas utilisé par les utilisateurs standards.
- *CMD* : La commande qui a lancé le processus.

- Afficher tous les processus en cours d'éxécution sur le système
```bash
ps -e
et
ps -ef
Détaille plus les processus en cours d'éxécution
```

---
## La gestion des paquets
La plupart des commandes de gestion de paquet nécessitent un accès *sudo* 

- Réactualisé la liste des paquets dispo
```bash
sudo apt-get update [paquets]
```

- Rechercher des mots-clés dans des paquets
```bash
apt-cache search [mot-clé]
```

- Installer des paquets
```bash
sudo apt-get install [paquets]
```

- Mise a jour des paquets
```bash
sudo apt-get upgrade [paquets]
```

- Supression de paquets
Supprimer un paquet
```bash
sudo apt-get remove [paquets]
```

Purger un paquet du système
```bash
sudo apt-get purge [paquets]
```
---
## MAJ des MPP utilisateur
On peut changer un mpd seulement sur l'utilisateur sur leqeul on est.
```bash
passwd
```

- Connaitre l'état de son mpd actuel
```bash
passwd -s sysadmin
```

- Le compte root peut modifier le mdp de n'importe quel utilisateur
```bash
passwd sysadmin
```


