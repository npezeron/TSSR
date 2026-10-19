# Glossaire de l'IA

## Concepts fondamentaux
- **AGI (intelligence artificielle générale)** : IA hypothétique capable d'accomplir n'importe quelle tâche intellectuelle humaine, et non une seule tâche précise.
- **algorithme** : suite d'instructions précises permettant de résoudre un problème ou d'effectuer un calcul.
- **apprentissage** : processus par lequel un modèle améliore ses performances à partir de données plutôt que de règles écrites à la main.
- **Attention (mécanisme d'attention)** : technique qui permet à un modèle de pondérer l'importance des différents éléments d'un texte pour comprendre le contexte.
- **auto-apprentissage** : capacité d'un système à apprendre seul, sans supervision humaine directe (ex. : à partir de données non étiquetées).
- **Biais (statistique et éthique)** : écart systématique dans les résultats d'un modèle, dû aux données ou à la conception, qui peut créer des discriminations.
- **capacité** : ce qu'un modèle est capable de faire (traduire, coder, raisonner, etc.).
- **Deep learning (apprentissage profond)** : apprentissage automatique reposant sur des réseaux de neurones à de nombreuses couches.
- **Embedding (plongement vectoriel)** : représentation d'un mot, d'une phrase ou d'une image sous forme de vecteur de nombres, où la proximité reflète la similarité de sens.
- **génératif** : se dit d'une IA qui produit du contenu nouveau (texte, image, son, code).
- **hallucination** : réponse fausse ou inventée, présentée par le modèle avec assurance.
- **IA faible / IA forte** : l'IA faible est spécialisée dans une tâche précise ; l'IA forte désigne une intelligence généraliste comparable à celle de l'humain.
- **Limite** : ce qu'un modèle ne sait pas ou ne peut pas faire de façon fiable (erreurs, connaissances figées, contexte borné).
- **Machine Learning** : apprentissage automatique, branche de l'IA où les machines apprennent à partir d'exemples.
- **mathématique** : discipline sur laquelle reposent les modèles d'IA (algèbre linéaire, probabilités, statistiques, calcul différentiel).
- **Multimodal** : se dit d'un modèle capable de traiter plusieurs types de données (texte, image, audio, vidéo).
- **Neurone / couche** : un neurone est une petite unité de calcul ; une couche est un ensemble de neurones traitant l'information à la même étape du réseau.
- **NLP (traitement du langage naturel)** : domaine de l'IA consacré à la compréhension et à la génération du langage humain.
- **Réseau neuronal** : modèle inspiré du cerveau, composé de couches de neurones artificiels reliés entre eux.
- **Reconnaissance vocale** : conversion de la parole en texte par une machine.
- **Rétropropagation** : algorithme d'entraînement qui calcule l'erreur en sortie puis la propage en sens inverse pour ajuster chaque poids.
- **Surapprentissage (overfitting)** : le modèle mémorise ses données d'entraînement au point de mal généraliser sur de nouvelles données.
- **Test de Turing** : test proposé par Alan Turing, où une machine réussit si un humain ne parvient pas à la distinguer d'une personne dans une conversation.
- **Transformer** : architecture de réseau de neurones basée sur l'attention, à l'origine des LLM actuels.
- **Vecteur / base de données vectorielle** : un vecteur est une liste de nombres ; une base vectorielle les stocke pour retrouver rapidement les éléments au sens proche.
- **Vision par ordinateur** : domaine de l'IA qui permet aux machines d'analyser et de comprendre des images ou des vidéos.

## Modèles et entraînement
- **base de données** : ensemble organisé d'informations stockées pour être consultées et exploitées.
- **Benchmark** : test standardisé servant à mesurer et comparer les performances des modèles.
- **Données d'entraînement / jeu de données** : ensemble d'exemples à partir desquels un modèle apprend.
- **Données synthétiques** : données générées artificiellement (souvent par une IA) pour entraîner ou tester des modèles.
- **distillation** : technique où un petit modèle apprend à imiter un modèle plus grand pour être plus léger et rapide.
- **Fenêtre de contexte** : quantité maximale de texte (en tokens) qu'un modèle peut prendre en compte en une fois.
- **Fine-tuning (ajustement fin)** : réentraînement d'un modèle existant sur des données spécifiques pour l'adapter à une tâche.
- **frontière (modèle)** : modèle à la pointe des capacités actuelles, parmi les plus puissants du moment.
- **inférence** : phase d'utilisation d'un modèle déjà entraîné pour produire une réponse.
- **Latence** : délai entre la requête et la réponse du modèle.
- **LLAMA** : famille de modèles de langage développée par Meta, diffusée avec des poids ouverts.
- **LLM** : grand modèle de langage, entraîné sur d'énormes quantités de texte pour comprendre et générer du langage.
- **Mixture of Experts (MoE)** : architecture où seuls certains sous-réseaux « experts » sont activés selon la requête, ce qui réduit le coût de calcul.
- **Open source / open weights** : modèle dont le code (open source) ou les poids (open weights) sont publiquement accessibles.
- **Paramètre** : valeur interne ajustée pendant l'entraînement ; le nombre de paramètres indique la taille du modèle.
- **poids** : paramètres numériques qui déterminent la force des connexions entre neurones et contiennent ce que le modèle a appris.
- **Pre-trained** : pré-entraîné, c'est-à-dire déjà entraîné sur un large corpus avant d'être adapté à un usage précis.
- **Quantification** : réduction de la précision numérique des poids pour alléger le modèle et accélérer son exécution.
- **RLHF (apprentissage par renforcement avec retour humain)** : méthode où des évaluations humaines servent à orienter le modèle vers des réponses plus utiles et sûres.
- **Scaling laws (lois d'échelle)** : observations montrant que les performances progressent de façon prévisible avec la taille du modèle, des données et du calcul.
- **token** : unité de texte (mot, morceau de mot, signe) traitée par un modèle de langage.
- **wikipedia** : encyclopédie en ligne, source très utilisée dans les données d'entraînement des modèles.

## Usages et ingénierie
- **agent** : système d'IA capable de planifier et d'enchaîner des actions de façon autonome pour atteindre un objectif.
- **API** : interface permettant à un logiciel d'accéder aux fonctions d'un autre, par exemple à un modèle d'IA.
- **automatisation** : exécution de tâches répétitives par des machines ou des logiciels sans intervention humaine.
- **autonomie** : degré auquel un système agit seul, sans validation humaine à chaque étape.
- **Chain of thought (raisonnement pas à pas)** : technique où le modèle détaille son raisonnement étape par étape, ce qui améliore souvent la qualité des réponses.
- **Copilote / assistant** : IA qui accompagne l'utilisateur dans une tâche (rédaction, code, etc.) sans la réaliser seule.
- **écoute** : captation de sons ou de conversations par un appareil ou une IA, posant des questions de vie privée.
- **environnement** : cadre dans lequel un agent agit et reçoit des retours (ou, selon le contexte, impact écologique de l'IA).
- **Function calling / tool use** : capacité d'un modèle à appeler des fonctions ou outils externes (recherche, calcul, base de données).
- **harnais** : infrastructure logicielle entourant un modèle (outils, mémoire, boucle d'exécution) pour en faire un agent ou l'évaluer.
- **injection** : attaque (prompt injection) qui glisse des instructions malveillantes dans les données pour détourner le comportement du modèle.
- **MCP (Model Context Protocol)** : protocole ouvert standardisant la connexion des modèles à des outils et sources de données.
- **OpenClaw** : agent IA personnel open source, capable d'agir sur l'ordinateur et les services de l'utilisateur.
- **OpenRouter** : plateforme proposant un accès unifié à de nombreux modèles d'IA via une seule API.
- **prompt** : instruction ou question donnée à un modèle d'IA.
- **Prompt engineering** : art de rédiger des prompts efficaces pour obtenir de meilleurs résultats.
- **RAG** : génération augmentée par récupération ; le modèle va chercher des documents pertinents avant de répondre.
- **Robotisation** : remplacement ou assistance de tâches humaines par des robots.
- **SLOP** : contenu de faible qualité généré en masse par IA et diffusé en ligne.
- **System prompt** : instructions de fond données au modèle qui définissent son rôle et son comportement.
- **vérification** : contrôle de l'exactitude des réponses d'une IA, notamment pour détecter les hallucinations.
- **Vibe coding** : programmation où l'on décrit ce que l'on veut en langage naturel et où l'IA écrit l'essentiel du code.

## Matériel et infrastructure
- **Calcul (compute)** : puissance de calcul nécessaire pour entraîner et faire fonctionner les modèles.
- **CUDA** : plateforme de NVIDIA permettant d'utiliser les GPU pour le calcul général, dont l'IA.
- **Datacenter** : centre de données regroupant les serveurs qui hébergent et exécutent les modèles.
- **FLOPS** : opérations en virgule flottante par seconde, unité de mesure de la puissance de calcul.
- **GPU** : processeur graphique, très efficace pour les calculs parallèles de l'IA.
- **Mémoire unifiée** : mémoire partagée entre CPU et GPU, évitant les copies de données entre les deux.
- **Puce / semi-conducteur** : composant électronique à la base de tous les processeurs, dont ceux de l'IA.
- **RAM(DRAM)** : mémoire vive de l'ordinateur, rapide mais volatile, où sont chargées les données en cours d'utilisation.
- **TPU** : processeur conçu par Google spécifiquement pour les calculs d'IA.
- **VRAM** : mémoire dédiée du GPU, qui limite la taille des modèles exécutables.

## Risques, éthique et société
- **AI Act (règlement européen)** : règlement de l'Union européenne qui encadre les systèmes d'IA selon leur niveau de risque.
- **alignement** : effort pour que les objectifs et comportements d'une IA correspondent aux valeurs et intentions humaines.
- **Biais algorithmique** : résultats systématiquement défavorables à certains groupes, hérités des données ou de la conception.
- **bulle IA** : crainte que les investissements et valorisations dans l'IA dépassent la valeur économique réelle.
- **cyberattaque par IA** : attaque informatique conçue, automatisée ou facilitée par une IA.
- **danger** : risque que l'IA cause des dommages, qu'ils soient immédiats (désinformation) ou à long terme.
- **Deepfake** : image, vidéo ou voix truquée de façon très réaliste par IA.
- **Désinformation** : diffusion volontaire de fausses informations, que l'IA peut produire à grande échelle.
- **Droit d'auteur / propriété intellectuelle** : questions juridiques sur l'usage d'œuvres protégées pour entraîner des modèles et sur la propriété des contenus générés.
- **Explicabilité / boîte noire** : difficulté à comprendre pourquoi un modèle produit telle réponse ; l'explicabilité vise à y remédier.
- **gouvernance** : règles, institutions et pratiques encadrant le développement et l'usage de l'IA.
- **Impact énergétique / empreinte carbone** : consommation d'électricité, d'eau et émissions liées à l'entraînement et à l'usage de l'IA.
- **invasif** : se dit d'une technologie qui s'immisce dans la vie privée ou les données personnelles.
- **Jailbreak** : technique visant à contourner les protections d'un modèle pour lui faire produire du contenu interdit.
- **Remplacement des emplois** : risque que l'IA et l'automatisation suppriment ou transforment des métiers.
- **Sécurité de l'IA (AI safety)** : domaine visant à prévenir les comportements dangereux ou imprévus des systèmes d'IA.
- **singularité technologique** : point hypothétique où l'IA dépasserait l'intelligence humaine et s'améliorerait seule, rendant l'avenir imprévisible.
- **souveraineté** : capacité d'un pays ou d'une organisation à maîtriser ses propres technologies, données et infrastructures d'IA.
- **super intelligence** : intelligence hypothétique largement supérieure à celle des meilleurs humains dans tous les domaines.
- **Vie privée / RGPD** : protection des données personnelles ; le RGPD est le règlement européen qui l'encadre.

## Acteurs et produits
- **Anthropic** : entreprise américaine d'IA, créatrice de Claude, axée sur la sécurité.
- **ChatGPT** : assistant conversationnel d'OpenAI.
- **Claude** : famille de modèles et assistant d'IA développés par Anthropic.
- **Gemini** : famille de modèles d'IA de Google.
- **Google DeepMind** : laboratoire de recherche en IA de Google.
- **HuggingFace** : plateforme et communauté de partage de modèles, de jeux de données et d'outils open source.
- **Meta** : entreprise à l'origine des modèles LLaMA.
- **Mistral** : entreprise française de modèles d'IA, avec des modèles ouverts et commerciaux.
- **NVIDIA** : fabricant de GPU, acteur central du matériel pour l'IA.
- **OpenAI** : entreprise américaine d'IA, créatrice de ChatGPT.