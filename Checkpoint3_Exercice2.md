# Partie 1 Gestions des Utilisateurs

## Q 2.1.1 

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/211/Capture%20d'%C3%A9cran%202023-12-22%20101946.png?raw=true)

## Q 2.1.2

Non Traité

# Partie 2 Configuration SSH

On va modifié le fichier "/etc/ssh/sshd_config" pour y rajouter la ligne suivante : "PermitRootLogin no"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/221/Capture%20d'%C3%A9cran%202023-12-22%20102410.png?raw=true)

On vérifie aussi le fichier
"/etc/ssh/sshd_config.d/local.conf"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/221/Capture%20d'%C3%A9cran%202023-12-22%20110426.png?raw=true)
On effectue un "systemctl restart ssh"
Si l'on essaye après ca on obtient le message suivant :

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/221/Capture%20d'%C3%A9cran%202023-12-22%20102545.png?raw=true)

## Q 2.2.2
On va modifié le fichier "/etc/ssh/sshd_config" pour y rajouter la ligne suivante : "AllowUsers vincent"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/221/Capture%20d'%C3%A9cran%202023-12-22%20102410.png?raw=true)

on effectue un "systemctl restart ssh"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/222/Capture%20d'%C3%A9cran%202023-12-22%20102712.png?raw=true)

## Q 2.2.3
Non Traité

# Partie 3 Analyse du Stockage

## Q 2.3.1

Grace a la capture d'écran suivante on en déduis que :

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/231/Capture%20d'%C3%A9cran%202023-12-22%20111348.png?raw=true)

Le volume md0p1 est monté sur /boot

Le volume logique Root est monté sur /

## Q 2.3.2

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/231/Capture%20d'%C3%A9cran%202023-12-22%20111348.png?raw=true)

le volume md0P1 utilise le systeme de stockage de type Raid 1

Le volume logique root utilise du LVM

## Q 2.3.3

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/233/Capture%20d'%C3%A9cran%202023-12-22%20122357.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/233/Capture%20d'%C3%A9cran%202023-12-22%20122534.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/233/Capture%20d'%C3%A9cran%202023-12-22%20122602.png?raw=true)

## Q 2.3.4 

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/234/Capture%20d'%C3%A9cran%202023-12-22%20120412.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/234/Capture%20d'%C3%A9cran%202023-12-22%20120450.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/234/Capture%20d'%C3%A9cran%202023-12-22%20120358.png?raw=true)

## Q 2.3.5
On constate grace a vgdisplay qu'il reste moins de 1.79gib sur notre volume groupe
![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P2/235/Capture%20d'%C3%A9cran%202023-12-22%20120608.png?raw=true)

# Partie 4 Sauvegardes

Non Traité

# Partie 5 Filtrage et analyse Réseau

Non Traité
# Partie 6 Analyse de log

Non Traité