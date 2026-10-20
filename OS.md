# OS

## Un peu d’histoire

**1970:** Création du système UNIX  
**1978:** Premier BSD, « fils » d’UNIX, qui donne naissance à plusieurs systèmes

1. FreeBSD (1993)
2. NetBSD (1993)
3. OpenBSD (1995)

**1980:** Naissance de XENIX  
**1981-2000:** Naissance de MS-DOS -> Fait important : le principal défaut de MS-DOS est qu’il est mono-utilisateur et mono-tâche  
**1985:** Naissance de Windows ([timeline](https://claude.ai/artifact/DPUE8vq3YigDmFHQAya7hy))  
**1991:** Naissance de GNU/Linux  
**2001:** Naissance de Mac OS X, issu de NeXTSTEP et de FreeBSD, dont découlera ensuite iOS (2007)  
**2008:** Naissance d’Android (annoncé en 2007)

## De quoi a besoin un ordinateur

Un ordinateur a besoin d’au moins 3 couches pour fonctionner.

### 1. Hardware

Un PC a besoin d’au minimum 4 composants hardware pour fonctionner :

1. CPU
2. RAM
3. Carte mère
4. Alimentation

Ces quatre composants appartiennent à la couche hardware.

### 2. Firmware

Ensuite il y a la deuxième couche, le **firmware** (BIOS ou UEFI), qui est composé de 2 parties :

1. POST : Power-On Self-Test
2. BIOS / UEFI

Le BIOS (ou l’UEFI) exécute le POST, puis lance l’OS.

### 3. OS

Plusieurs OS sont apparus au fil des années, de BSD à Windows et macOS. Beaucoup sont inspirés d’UNIX, mais pas Windows.

## Les puces

| Date | Nom de la puce | Fréquence | Architecture | Nb de cœurs | Bits | Débit |
|------|:--------------:|:---------:|:------------:|:------------|:----:|:------|
| 1986 | Intel 286-12 | 12 MHz | CISC | 1 cœur | 16 bits | 24 Mo/s |
| 2000 | Intel P4 | 1,4 GHz | CISC | 1 cœur | 32 bits | 5,2 Go/s |
| 2011 | Core Duo Extreme | 3,2 GHz | CISC | Dual core + HT | 64 bits | 112 Go/s |
| 2021 | Core i7 | 3,8 GHz | CISC | 8 cœurs + HT | 64 bits | 243 Go/s |
| Top 2026 | Intel serveur quadriprocesseur | 3,2 GHz | CISC | 288 cœurs, pas HT | 64 bits | 28 To/s |