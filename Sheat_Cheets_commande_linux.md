
### Cheat sheet — Commandes Linux

#### Navigation et fichiers

| Commande | Description |
|----------|-------------|
| `pwd` | Affiche le dossier courant |
| `ls -la` | Liste les fichiers (détails + fichiers cachés) |
| `cd /chemin` | Change de dossier (`cd ..` remonte, `cd ~` va au dossier personnel) |
| `mkdir -p dossier/sous-dossier` | Crée un dossier (et les parents) |
| `touch fichier` | Crée un fichier vide |
| `cp -r source dest` | Copie un fichier ou un dossier |
| `mv source dest` | Déplace ou renomme |
| `rm fichier` / `rm -r dossier` | Supprime (attention : pas de corbeille) |

#### Lecture et recherche

| Commande | Description |
|----------|-------------|
| `cat fichier` | Affiche le contenu |
| `less fichier` | Affiche page par page (`q` pour quitter) |
| `head -n 20 fichier` / `tail -n 20 fichier` | Début / fin du fichier |
| `tail -f fichier` | Suit un fichier en temps réel (logs) |
| `grep "motif" fichier` | Cherche un texte (`-r` récursif, `-i` sans casse) |
| `find /chemin -name "*.conf"` | Cherche des fichiers par nom |
| `wc -l fichier` | Compte les lignes |

#### Droits et propriétaires

| Commande | Description |
|----------|-------------|
| `chmod 644 fichier` | Modifie les droits (r=4, w=2, x=1) |
| `chmod +x script.sh` | Rend un fichier exécutable |
| `chown user:groupe fichier` | Change le propriétaire et le groupe |
| `sudo commande` | Exécute avec les droits administrateur |
| `su - utilisateur` | Bascule vers un autre utilisateur |

#### Utilisateurs et groupes

| Commande | Description |
|----------|-------------|
| `whoami` / `id` | Utilisateur courant et ses groupes |
| `adduser nom` | Crée un utilisateur |
| `passwd nom` | Change un mot de passe |
| `usermod -aG groupe nom` | Ajoute un utilisateur à un groupe |
| `deluser nom` | Supprime un utilisateur |

#### Processus et ressources

| Commande | Description |
|----------|-------------|
| `ps aux` | Liste tous les processus |
| `top` / `htop` | Suivi en temps réel (CPU, RAM) |
| `kill PID` / `kill -9 PID` | Arrête un processus (`-9` = forcé) |
| `free -h` | Utilisation de la mémoire |
| `uptime` | Durée de fonctionnement et charge |

#### Services (systemd)

| Commande | Description |
|----------|-------------|
| `systemctl status service` | État d'un service |
| `systemctl start\|stop\|restart service` | Démarre, arrête, redémarre |
| `systemctl enable service` | Active au démarrage |
| `journalctl -u service -f` | Logs d'un service en direct |
| `journalctl -xe` | Dernières erreurs système |

#### Paquets (Debian / Ubuntu)

| Commande | Description |
|----------|-------------|
| `sudo apt update` | Met à jour la liste des paquets |
| `sudo apt upgrade` | Met à jour les paquets installés |
| `sudo apt install paquet` | Installe un paquet |
| `sudo apt remove paquet` | Supprime un paquet |
| `apt search mot` | Recherche un paquet |

#### Réseau

| Commande | Description |
|----------|-------------|
| `ip a` | Adresses IP des interfaces |
| `ip r` | Table de routage |
| `ping -c 4 hôte` | Teste la connectivité |
| `ss -tulnp` | Ports en écoute et processus associés |
| `dig domaine` / `nslookup domaine` | Résolution DNS |
| `traceroute hôte` | Chemin réseau vers une destination |
| `curl -I url` | Récupère les en-têtes HTTP |

#### Disques et espace

| Commande | Description |
|----------|-------------|
| `df -h` | Espace disque par partition |
| `du -sh dossier` | Taille d'un dossier |
| `lsblk` | Liste des disques et partitions |
| `mount` / `umount` | Monte / démonte un système de fichiers |

#### Archives et transferts

| Commande | Description |
|----------|-------------|
| `tar -czvf archive.tar.gz dossier` | Crée une archive compressée |
| `tar -xzvf archive.tar.gz` | Extrait une archive |
| `ssh user@hôte` | Connexion à distance |
| `scp fichier user@hôte:/chemin` | Copie via SSH |
| `rsync -avz source dest` | Synchronise des dossiers |

#### Pare-feu (UFW)

| Commande | Description |
|----------|-------------|
| `sudo ufw status` | État du pare-feu |
| `sudo ufw allow 22/tcp` | Autorise un port |
| `sudo ufw enable` | Active le pare-feu |

#### Astuces du terminal

| Raccourci | Description |
|-----------|-------------|
| `Tab` | Autocomplétion |
| `Ctrl + C` | Interrompt la commande en cours |
| `Ctrl + R` | Recherche dans l'historique |
| `!!` | Relance la dernière commande |
| `commande --help` / `man commande` | Aide sur une commande |
| `cmd1 \| cmd2` | Enchaîne (le résultat de cmd1 va dans cmd2) |
| `cmd > fichier` / `cmd >> fichier` | Écrit / ajoute la sortie dans un fichier |

---