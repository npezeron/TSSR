# Guide d'installation d'une instance LLM locale sur Debian 13

Ce guide détaille la méthode la plus rapide et efficace pour faire tourner un grand modèle de langage (LLM) en local sur **Debian 13 (Trixie)** en utilisant **Ollama**.

---

#### Étape 1 : Mettre à jour le système

Ouvrez votre terminal et assurez-vous que votre système est parfaitement à jour :

```bash
sudo apt update && sudo apt upgrade -y
```

---

#### Étape 2 : Installer Ollama

Ollama automatise la gestion et l'exécution des LLM. Installez-le à l'aide du script officiel :

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

> **Note :** Si la commande `curl` n'est pas installée sur votre machine, exécutez d'abord `sudo apt install curl -y`.

---

#### Étape 3 : Télécharger et lancer un modèle léger

Pour une configuration standard (8 Go à 16 Go de RAM), les modèles de taille réduite offrent un excellent compromis entre vitesse et pertinence.

Exécutez la commande suivante pour télécharger et lancer **Llama 3.2 (3B)** :

```bash
ollama run llama3.2
```

##### Alternatives recommandées

- **Très léger (PC modestes) :** `ollama run qwen2.5:1.5b`
- **Performant (Code & Logique) :** `ollama run phi3`

Une fois le téléchargement terminé, une invite de commande `>>>` apparaît. Vous pouvez directement chatter avec l'IA. Pour quitter, tapez `/bye`.

---

#### Étape 4 : (Optionnel) Installer une interface Web (Style ChatGPT)

Pour éviter d'utiliser le terminal à chaque fois, vous pouvez déployer **Open WebUI** via Docker.

##### 1. Installer Docker

```bash
sudo apt install docker.io -y
sudo systemctl enable --now docker
```

##### 2. Lancer le conteneur Open WebUI

Cette commande télécharge et configure l'interface Web en la connectant automatiquement à votre instance Ollama locale :

```bash
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

##### 3. Accéder à l'interface

Ouvrez votre navigateur web et rendez-vous à l'adresse suivante :
👉 [http://localhost:3000](http://localhost:3000)

*La première connexion nécessitera la création d'un compte administrateur local (vos données restent stockées sur votre machine).*

### Webographie

- [IA & Stratégie : Adieu les Apps : La nouvelle stratégie IA d'Apple qui vous concerne directement](https://www.youtube.com/watch?v=Pdfanhj0qsk)
- [Korben - Llama Windows LLM local](https://korben.info/llama-windows-llm-local.html)
- [TryHackMe - AI & ML Security Threats](https://tryhackme.com/room/aimlsecuritythreats)
- [CNIL - Glossaire IA](https://www.cnil.fr/fr/intelligence-artificielle/glossaire-ia)
- [CCI Touraine - Page 1](https://www.calameo.com/cci-touraine/read/00169748932cbc5e72e6c?page=1)
