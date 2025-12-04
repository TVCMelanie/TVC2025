# Gestion des logiciels et paquets sous linux
## La notion de paquets sous Linux
Sous Linux pour installer un logiciel, on doit installer des paquets logiciel.
---
- ign veut dire ignore, il n'arrive pas à faire les mise a jour
- apt et apt get- c'est la même chose

---
- Afficher le contenu d'un fichier, ici sources.list
```bash
cat /etc/apt/sources.list
```

- Liste des commandes avec l'outil de gestion des paquets
```bash
apt --help
```

- Mise à jour des sources des paquets et des paquets 
```bash
apt update && apt upgrade
```

- Effectue la mise à jour
```bash
apt upgrade
```

- Effectue les 2 dans la foulé
```bash
apt update && apt upgrade
```

- Installer de nouveaux paquets
```bash
apt install
```

- List l'ensemble des paquets installé
```bash
dpkg -l
```

- Ex : liste l'ensemble des paquets installés de VLC (donc vérifier l'install de VLC)
```bash
dpkg -l | grep vlc
```

- Supprimer le paquet vlc
```bash
apt remove vlc
```

- Supprime le paquet et ses configurations
```bash
apt purge vlc
```

- Supprimer avec les paquets orphelin (qui ne servent plus) de vlc
```bash
apt autoremove vlc
```

- On efface toutes traces de vlc
```bash
apt purge vlc && apt autoremove vlc
```

- On cherche l'existance existe pour ma distribution
```bash
apt search gimp
```

- Demandé de mettre à jour uniquement firefox
```bash
apt install --only-upgrade firefox-esr
```
apt upgrade --only... fait la même chose

- Demandé de mettre à jour uniquement firefox
```bash
apt install --only-upgrade firefox-esr
```
---
## Gestion des dépôts et sources de logiciels
- 
```bash

```
--- 
# Note de christophe
- Installer un logiciel à partir des dépots offiiel débian
```
apt install vlc
```

- Installer un logiciel à partir des dépôt d'un éditeur
```
Dans
cd /atc/apt/keyrings/
wget https://dl.google.com/linux/linux_signing_key.pub
mv linux_signing_key.pub google_key.pub
gpg --dearmor google_key.pub > google_key.gpg
echo deb [signed-by=/usr/share/keyrings/google-key.pub.gpg]
http://dl.google.com/linux/chrome/deb/stable main > /etc/apt/sources.list.d/google-chrome.list
apt update
apt install google-chrome-stable
```

- Installer un logiciel Discord manuellement à partir d'un fichier .deb
```
wget discord.deb https://discord.com/api/download?platform=linux&format=deb
dpkg -i discord.deb
si besoin :
apt --fix-broken install
```

## Configuration de l'horloge
- Syncronisation sur un serveur spécifique NTP : fichier /etc/systemd/timesyncd.conf
```conf
nona timesyncd.conf
[Time]
NTP=ntp.univ-rennes2.fr
FallbackNTP=0.debian.pool.ntp.org 1.debian.pool.ntp.org 2.debian.pool.ntp.org 3.debian.pool.ntp.org
```

- Activer NTP
```
timedatectl set-ntp true
```

- Vérifier la syncronisation
```
timedatectl timesync-status
```



- 
