# GOBUSTER


gobuster est un outil de brutforce pour l'enumeration de page web ecrit en go.

## Commande utils


```bash
gobuster dir -w /path/to/wordlist -u <ADRESSE>
```

La premiere commande permet de trouver des pages web, l'option -w est le chemin vers une wordlist (liste), l'option -u est l'adresse http(s) de la cible.
Cette commande est tres utile pour trouver des dossier


```bash
gobuster dir -w /path/to/wordlist -u <ADRESSE> -x <EXTENTION>
```

L'option -x permet elle de trouver des fichier, il suffit de preciser le(s) extention(s) separe par une "," par exemple : txt,php,md


