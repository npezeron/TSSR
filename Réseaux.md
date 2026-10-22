# Qu'est ce que le réseaux informatique

Un réseau informatique est un ensemble d’équipements (ordinateurs, serveurs, imprimantes, smartphones, objets connectés...) reliés entre eux, par des liaisons filaires ou sans fil, afin de communiquer et partager des ressources : données, fichiers, applications, accès à Internet, périphériques.

## Modéle OSI

### Définition du modèle OSI

Le modèle OSI est un modèle théorique normalisé par l’ISO qui décrit comment les données circulent entre deux systèmes sur un réseau. Il découpe la communication en 7 couches empilées.

1. Physique : Bits (Câble)
2. Liason de donnée: Trame (Switch )
3. Réseaux: Paquet (Router)
4. Transport: Segment (TCP ou UDP)
5. Session: 
6. Présentation 
7. Application

 Les 3 dernières couche c'est là ou les données passe

## Modéle TCP/IP

### Définition du modèle TCP/IP

Le modèle TCP/IP (Transmission Control Protocol / Internet Protocol) est le modèle d’architecture réseau réellement utilisé sur Internet. Contrairement au modèle OSI, qui est surtout théorique, TCP/IP est issu d’une approche pratique : il s’est construit à partir des protocoles développés pour ARPANET dans les années 1970, puis s’est imposé comme standard de fait.

1. Accès au réseaux: Couche OSI 1,2  
2. Internet: Couche OSI 3
3. Transport: Couche OSI 4
4. Application: Couche OSI 5,6,7

 ### Norme IEEE

- 802.3 (Ethernet) c'est la norme des câbles RJ45
  - LAN MAN WAN ce sont les différent type de réseaux 

- 802.11 (Wifi) c'est la norme WIFI
  - SOHO small Office Home Office

# Windows serveur

## Définition 

Windows serveur est un OS qui fournis des services, comme un AD, DNS, DHCP etc.

### Un peu d'hitsoire

1. **RIS 2000-2003:** Ancètre du WDS il permet de copier un secteur d'un disque dur, mais trop rigide car il faut exactement les même machine pour pouvoir déployer un ISO depuis le serveur

2. **WDS duo et MDT 2005-2023:**
   - **WDS** servait de "tuyau" (transort réseau)
   - **MDT**servait de "cerveau" (automatisation, pilotes,logiciels)

3. La Transition Actuelle: La fin de MDT

-> Microsoft a officellement arrêté le développement de MDT. Il n'est plus supporté pour Windows 11

-> MDT ne gère pas nativement mes bios UEFI modernes, le Secure Boot et le architecutures Cloud

### Pourquoi le WDS et 2026 alors ?

Même si MDT s'efface, le WDS reste essentiel pour deux raisons:

- **L'infrastructure mocale:** Dans les environnements isolé d'Internet ( usines, banques, défense), le Cloud n'est pas une option. Le WDS reste le seul moyen de déloyer.

- **Le dépannage:** Savoir amorcer une machine via le réseu reste une compétence de base pour n'importe quel administrateur système.

**C'est une technologie qui a posé les bases de l'automatisation

## PXE: Preboot eXecution Environment

### Définition

Standard permettant à une station de démarrer depuis le réseau avant même d'avoir un OS sur son disque

### Fonctionnement général

1. Le client envoue une requête DHCP "Discovery".

2. Le serveur DHCP répond avec une IP et les "Option PXE" (Option 66 et 67).

3. Le client contacte le serveur WDS pour télécharger le programme d'amorce.

## PXE en détail

### Phase 1: Découverte (DHCP -> D.O.R.A)

Le Client envoie un paquet DHCP Discover avec une option spécifique (Option 93) qui indique qu'il est un client PXE et précise son architecture (BIOS x86, UEFI x64, ou ARM64).  

Le Serveur DHCP répond avec une adresse IP avec les Option 66 (Nom d'hôte du serveur de démarrage) et 67 (Nom du fichier de démarrage, ex: bootmgfw.efi)

**D.O.R.A** 

1. Discover
2. Offer
3. Request
4. Acknowlegde

### Phase 2: Transfert TFTP

Une fois l'adresse du serveur WDS connue, le client utilise le protocole TFTP (Trivial File Transfer Protocol) sur le port 69. Protocole simple et léger, capable de fonctionner alors que le PC n'a encore aucun pilote complexe chargé en mémoire, le client télécharge le NBP (Network Boot Program).

### Phase 3: Exécution du NBP

Le programme de démarrage (wdsndb.com pour le BIOS ou wdsmgf.efi pour l'UEFI) s'exécute en RAM. L'utilisateur voi alors le message comme: "Press F12 for network boot".