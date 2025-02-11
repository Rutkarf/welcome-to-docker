🐳 Exercice Docker - Jour 1 : Welcome to Docker
Docker Logo
📚 Table des matières

    🌟 Introduction
    🛠️ Prérequis
    💻 Installation de Docker
    ✅ Vérification de l'installation
    🔍 Récupération de l'image Docker
    🏗️ Construction et exécution du conteneur
    🛑 Arrêt et suppression du conteneur
    🗑️ Suppression de l'image
    🧰 Commandes Docker utiles
    🎓 Conclusion

🌟 Introduction
Plongez dans l'univers de Docker avec cet exercice pratique ! Nous explorerons les fondamentaux, de l'installation à l'exécution d'un conteneur simple, en utilisant l'image welcome-to-docker.
🛠️ Prérequis

    💻 Un système d'exploitation compatible (Windows, macOS, Linux)
    🔑 Accès administrateur sur votre machine
    🌐 Connexion Internet stable

💻 Installation de Docker

    📥 Téléchargez Docker Desktop depuis le site officiel.
    🚀 Suivez les instructions d'installation pour votre système d'exploitation.

    💡 Astuce Pro : Sur Windows, activez WSL2 pour des performances optimales ! 

✅ Vérification de l'installation
Après l'installation, ouvrez votre terminal préféré et exécutez ces commandes magiques :

```bash
$ docker --version
Docker version 27.4.0, build bde2b89
```

```
$ docker info
Client:
 Version:    27.4.0
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  ai: Ask Gordon - Docker Agent (Docker Inc.)
    Version:  v0.5.1
    Path:     C:\Program Files\Docker\cli-plug
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.19.2-desktop.1
    Path:     C:\Program Files\Docker\cli-plug
  # ... (autres plugins)

Server:
ERROR: error during connect: Get "http://%2F%2/pipe/dockerDesktopLinuxEngine: Le fichier spé
errors pretty printing info

```

```
$ docker ps
error during connect: Get "http://%2F%2F.%2Fpi //./pipe/dockerDesktopLinuxEngine:
```

```
$ docker images
error during connect: Head "http://%2F%2F.%2FprDesktopLinuxEngine: Le fichier spécifié est introuvable 
```

    ⚠️ Attention : Si des erreurs surgissent, vérifiez que Docker Desktop tourne en arrière-plan ! 

🔍 Récupération de l'image Docker
Embarquez l'image "welcome-to-docker" avec cette incantation :


```
bash
$ docker pull docker/welcome-to-docker
Using default tag: latest
error during connect: Post "http://%2F%2F.%2Fpge=docker%2Fwelcome-to-docker&tag=latest": opest introuvable.
```


🏗️ Construction et exécution du conteneur
Lancez votre premier conteneur avec cette commande magique :

```
bash
$ docker run -it --rm -p 8080:80 docker/welcome-to-docker
```


🌐 Naviguez vers
text
http://localhost:8080
et admirez votre création !
🛑 Arrêt et suppression du conteneur
Pour arrêter votre conteneur, utilisez la combinaison secrète
text
Ctrl+C
ou cette commande :

```
bash
$ docker stop $(docker ps -q --filter ancestor=docker/welcome-to-docker)
```


🗑️ Suppression de l'image
Effacez les traces de votre aventure Docker :

```
bash
$ docker rmi docker/welcome-to-docker
```


🧰 Commandes Docker utiles
Commande	Description
text
docker ps
	📋 Liste les conteneurs en cours d'exécution
text
docker images
	🖼️ Affiche les images Docker disponibles
text
docker rm
	🗑️ Supprime un ou plusieurs conteneurs
text
docker rmi
	🧹 Efface une ou plusieurs images

    🔍 Pro Tip : Explorez toutes les commandes avec

    text
    docker --help
    ! 

🎓 Conclusion
Bravo, apprenti Docker ! 🎉 Vous avez maintenant les bases pour naviguer dans l'océan des conteneurs. Continuez à explorer et à expérimenter avec différentes images et configurations. 📚 Ressources pour aller plus loin :

    📘 Documentation officielle Docker
    🏗️ Docker Hub
    📜 Docker Cheat Sheet
