# RSNYC


## Qu'est ce que rsync ?

rsync remote synchronization, en français : « synchronisation distante » est un logiciel libre de synchronisation de fichiers, distribué sous licence GNU GPL


## Commande utile

La commande rsync permet principalement la synchronisation mais avant il faut savoir les fichier et dossier présent sur la machine distante :

```bash
rsync --list-only -a rsync://10.129.234.169/
	backups        	backups
```

Les options utiliées sont :
	- --list-only : affiche uniquement les fichiers disponibles, sans les transférer.
	- -a : normalement utilisée pour les transferts en mode archive.


```bash
rsync -a rsync://10.129.234.169/backups/jenkins.tar.gz .
```
Maintenant nous avons réaliser la synchronisation de /backups/jenkins.tar.gz de la machine 10.129.234.169 dans le repertoire . de la machine physique
