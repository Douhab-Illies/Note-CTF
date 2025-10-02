#FFUF

## Qu'est ce que ffuf ?

ffuf est un outil de fizzing, il permet de tester des requete pour faire de l'enumeration de fichier, repertoire, ou de sous-domaine.

## Commande utils

```bash
ffuf -u http://FUZZ.editor.htb -w /usr/share/wordlists/seclists/Discovery/DNS/namelist.txt
```

Cette premiere commande peremt de faire de l'enumeration de sous-domaine, l'outil va remplacer "FUZZ" par les element de wordlist "-w".



