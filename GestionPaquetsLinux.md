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

- Mise à jour des lists des paquets à mettre à jour
```bash
apt update
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
