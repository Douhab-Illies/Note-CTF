# SCAN

Dans un CTF la premiere etape est le scan de la machine. On va commencer par enumerer les services accessible sur la machine

## SCAN DE PORTS

La premiere commande a lancer est **nmap**
Cela permet de voir les services et ports ouvert sur la machine.

Les premiers ports a verifier sont :

- 21 / FTP
- 22 / SSH
- 80 / 8080 /HTTP (web)
- 443 / HTTPS (web)
- 445 / SMB

Le plus important est chercher si les vesrions des services ont une vulnerabilite ( l'option -A est importante )


### FTP

Si un serveur FTP est present sur la machine cible la premiere chose a faire est de tester la connection en anymous :

```bash
ftp anonymous@<IP>
```

Si un mot de passe est requis, il faudra tester anonymous

Dans le cas un authentification reussite, il faut conaitre plusieurs commande : 

- ls / lister les fichier 
- get / recuperer un fichier sur sa machine physique
- less / more / pour lire un fichier depuis le shell du ftp
- cd / se deplacer dans le dossiers
- put /  pour ajouter un fihcier sur le serveur ftp


### SMB

Si un serveur SMB est present sur la machine cible la premiere chose a faire est de lister les partage de fichier : 

```bash
smbclient -N -L //<IP>
```

Si des partages sont presents, il est possible de tester la connexion avec un compte anonyme : 

```bash
smbclient -N //10.10.100.44/<PARTAGE>
```

Dans le cas un authentification reussite, il faut conaitre plusieurs commande :

- ls / lister les fichier
- get / recuperer un fichier sur sa machine physique
- less / more / pour lire un fichier depuis le shell du smb
- cd / se deplacer dans	le dossiers
- put /  pour ajouter un fihcier sur le serveur smb



### HTTP
L'une des première choses a regarder est le serveur et sa version.
Une fois cela fait, il faut impérativement verfier si une vulnérabilité existe.

