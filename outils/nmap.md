# NMAP 

## Qu'est ce que nmap ?

Nmap est un scanner de ports libre créé par Fyodor et distribué par Insecure.org. Il est conçu pour détecter les ports ouverts, identifier les services hébergés et obtenir des informations sur le système d'exploitation d'un ordinateur distant.


## Commande utils

```bash
nmap <IP>
```

Cette simple commande permet de scanner les 1024 premier ports

```bash
nmap -p- <IP>
```

Cette commande elle va scanner les 65535 ports. On peut scanner un port precis en remplacant le deuxieme '-' apres le 'p' et le remplacer soit par un port precis ou par une plage de port

```bash
nmap -p80 <IP>
nmap -p80-1024 <IP>
```

L'une des options les plus utils reste le -A, elle permet d'obtenir des information tels que : le systeme d'exploitation utilise, les versions des services qui sont accessible ...

```bash
nmap -A <IP>
```

Si les scans sont trop long, il est possible de resuire ce temps en utilisant -T suivi d'une valeur comprise entre 0-5. Plus la valeur est haute plus le scan sera rapide.

```bash
nmap -T<0-5> <IP>
```



## La commande ultime

En conclusion, la commande ultime de scan NMAP est 

```bash
nmap -A -p- -T5 <IP>
```



script par ex smb

nmap 10.10.10.4 --script="smb-vuln*"
