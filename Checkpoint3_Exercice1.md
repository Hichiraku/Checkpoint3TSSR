# Partie 1 : Gestion des Utilisateurs

## Q 1.1.1 
Pour crée le nouvel utilisateur Lionel.Lemarchand on va faire un clique droit sur Kelly.rhameur > Copy afin de récupérer plus rapidement ses attributs de société.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/111/Capture%20d'%C3%A9cran%202023-12-22%20092557.png?raw=true)

On renseigne manuellement ses informations.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/111/Capture%20d'%C3%A9cran%202023-12-22%20092627.png?raw=true)

Ainsi que son mot de passe, on coche la case "**User must change password at next logon**" car nous voulons qu'il utilise un mot de passe personnel qui respectera les critères de mots de passe de notre société.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/111/Capture%20d'%C3%A9cran%202023-12-22%20092908.png?raw=true)

Enfin on complète manuellement son "**Job Title**" qui n'as pas été renseigné automatiquement au moment de la copie.

## Q 1.1.2
Pour désactiver l'utilisateur Kelly.Rhameur, on se rend dans les propriétés de son objetAD, dans l'onglet "**Account**" et on coche la case "**Account is disabled**".

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/112/Capture%20d'%C3%A9cran%202023-12-22%20093000.png?raw=true)

On va créer l'OU DeactivatedUsers directement dans l'OU LabUsers.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/112/Capture%20d'%C3%A9cran%202023-12-22%20093054.png?raw=true)

Enfin il nous suffit de juste déplacer Mme Rhameur dans cette OU fraîchement créée.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/112/Capture%20d'%C3%A9cran%202023-12-22%20093149.png?raw=true)

## Q 1.1.3
On va modifier le groupe dans lequel Mme Rhameur etait présente, dans l'onglet "**Members**" on "**Remove**" simplement son compte du groupe. Et comme M Lemarchand à été crée directement par la copie de Mme Rhameur, il est automatiquement présent dans ce groupe.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/113/Capture%20d'%C3%A9cran%202023-12-22%20093238.png?raw=true)

## Q 1.1.4
On créer simplement le dossier de M Lemarchand dans le volume prévue à cette effet, dans notre cas le "**F:**", on configurera son accès au niveau de la Parti 3

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/114/Capture%20d'%C3%A9cran%202023-12-22%20093743.png?raw=true)

## Q 1.2.1
Pour empêcher M Ghul de se connecter en dehors de ses heures de travail, il nous suffit de se rendre dans les propriété de son objetAD, dans l'onglet "**Account**" et on clique sur le bouton "**Logon Hours**"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/121/Capture%20d'%C3%A9cran%202023-12-22%20094400.png?raw=true)

Et on séléctionne les heures pendant lesquelles M Ghul pourra se connecter 

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/121/Capture%20d'%C3%A9cran%202023-12-22%20094515.png?raw=true)

## Q 1.2.2

Pour limiter sa connexion a un seul ordinateur on retourne au meme endroit que pour la Q 1.2.1 et cette fois on choisie l'option "**Log on to**"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/121/Capture%20d'%C3%A9cran%202023-12-22%20094400.png?raw=true)

On séléctionne l'option "**The following computer**" et on renseigne le nom de l'ordinateur auquel il est attribué, dans notre cas on renseigne le seul ordinateur du domain "**CLIENT01**"

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/122/Capture%20d'%C3%A9cran%202023-12-22%20094702.png?raw=true)

## Q 1.2.3
Pour  mettre en place la stratégie de mot de passe on se rend dans l'Administrative Center, dans celui ci on effectue le chemin suivant : "**TSSR>System>Password Settings Container**"
On renseigne dans cette politique de mot de passe les champs que l'on veut appliquer.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/123/Capture%20d'%C3%A9cran%202023-12-22%20094942.png?raw=true)

Pour facilité son application j'ai crée un groupe dans mon AD qui regroupe tout les groupes existant dans l'OU LabUsers

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/123/Capture%20d'%C3%A9cran%202023-12-22%20095756.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/123/Capture%20d'%C3%A9cran%202023-12-22%20095834.png?raw=true)

Enfin je l'applique directement a ma politique de mot de passe pour qu'elle soit effective sur tout les utilisateurs de mon AD

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/123/Capture%20d'%C3%A9cran%202023-12-22%20095949.png?raw=true)

## Q 1.3.1
On commence par crée une GPO dans le dossier prévu a cette effet, et on y ajoute le groupe précédemment crée pour qu'il s'applique à tout les utilisateurs de mon OU LabsUsers, ainsi qu'au groupe Domain Computer, sans ca la GPO ne fonctionnera pas

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20100209.png?raw=true)

Je désactive ensuite les "Computer configuration settings disabled" par bonne pratique, en effet notre GPO sera pour les utilisateurs et donc nous n'avons pas besoin des configuration ordinateurs

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20100221.png?raw=true)

On effectue ensuite la mise en partage réseaux du dossier New Folder dans le lecteur "E:\\**DossierCommun**" 

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20100608.png?raw=true)

On fait la même chose sur le disque F:

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20100811.png?raw=true)

On édite notre GPO pour y ajouter notre regle de mappage de lecteur 

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101018.png?raw=true)

On renseigne les informations nécessaires

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101205.png?raw=true)

Comme c'est une GPO qui agit sur les utilisateurs on active le Run in "Logged-on user's security"
![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101220.png?raw=true)

On fait la meme chose pour le lecteur F: sauf qu'on ajoute cette fois ci la variable %logonuser% pour que le mappage se fasse automatique sur le dossier de l'utilisateur.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101416.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101220.png?raw=true)

On vois que nos deux lecteurs sont mappé.

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101433.png?raw=true)

Il ne reste plus qu'a appliqué la GPO a l'OU LabUsers

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101456.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101504.png?raw=true)

![img](https://github.com/Hichiraku/Checkpoint3TSSR/blob/main/CKPNT3/CKPNT3P1/131/Capture%20d'%C3%A9cran%202023-12-22%20101518.png?raw=true)


