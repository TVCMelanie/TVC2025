# TP5 Charline
## Accessible en mode privilège root

- Ajouter un utilisateur avec son nom (ex : adduser Mélanie)
```bash
adduser
```

- Sortir d'un utilisateur quand on est en root
```bash
exit
```

- Se mettre en compte ajouter (ex compte ajouté Mélanie)
```bash
su - Mélanie
```

- Ajouter un utilisateur avec son nom et ses privilèges
```bash
useradd -d /home/alf2 -m -g stagiaire -G sudo -u 1002 alf2
```

- Supprimer un utilisateur et ses fichier avec la récursive
```bash
userdel -r alf2
```


