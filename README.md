# Exercice Docker - Jour 1 : Welcome to Docker

![Docker Logo](chemin/vers/votre/image/docker_logo.png)

## Table des matières
- [Introduction](#introduction)
- [Prérequis](#prérequis)
- [Installation de Docker](#installation-de-docker)
- [Vérification de l'installation](#vérification-de-l'installation)
- [Récupération de l'image Docker](#récupération-de-l'image-docker)
- [Construction et exécution du conteneur](#construction-et-exécution-du-conteneur)
- [Arrêt et suppression du conteneur](#arrêt-et-suppression-du-conteneur)
- [Suppression de l'image](#suppression-de-l'image)
- [Commandes Docker utiles](#commandes-docker-utiles)
- [Conclusion](#conclusion)

## Introduction

Cet exercice couvre les bases de Docker, de l'installation à l'exécution d'un conteneur simple. Nous utiliserons l'image [welcome-to-docker](https://github.com/docker/welcome-to-docker) pour nos tests.

## Prérequis

- Un système d'exploitation compatible (Windows, macOS, Linux)
- Accès administrateur sur votre machine
- Connexion Internet stable

## Installation de Docker

1. Téléchargez Docker Desktop depuis le [site officiel](https://www.docker.com/products/docker-desktop).
2. Suivez les instructions d'installation pour votre système d'exploitation.

> 💡 **Astuce** : Sur Windows, assurez-vous que WSL2 est activé pour de meilleures performances.

![Installation Docker](chemin/vers/votre/capture/installation_docker.png)

## Vérification de l'installation

Après l'installation, ouvrez un terminal et exécutez les commandes suivantes :

$ docker --version
Docker version 27.4.0, build bde2b89

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
  compose: Docker Compose (Docker Inc.)
    Version:  v2.31.0-desktop.2
    Path:     C:\Program Files\Docker\cli-plug
  debug: Get a shell into any image or contain
    Version:  0.0.37
    Path:     C:\Program Files\Docker\cli-plug
  desktop: Docker Desktop commands (Beta) (Doc
    Version:  v0.1.0
    Path:     C:\Program Files\Docker\cli-plug
  dev: Docker Dev Environments (Docker Inc.)
    Version:  v0.1.2
    Path:     C:\Program Files\Docker\cli-plug
  extension: Manages Docker extensions (Docker
    Version:  v0.2.27
    Path:     C:\Program Files\Docker\cli-plug
  feedback: Provide feedback, right in your te
    Version:  v1.0.5
    Path:     C:\Program Files\Docker\cli-plug
  init: Creates Docker-related starter files f
    Version:  v1.4.0
    Path:     C:\Program Files\Docker\cli-plug
  sbom: View the packaged-based Software Bill 
    Version:  0.6.0
    Path:     C:\Program Files\Docker\cli-plug
  scout: Docker Scout (Docker Inc.)
    Version:  v1.15.1
    Path:     C:\Program Files\Docker\cli-plug

Server:
ERROR: error during connect: Get "http://%2F%2/pipe/dockerDesktopLinuxEngine: Le fichier spé
errors pretty printing info

$ docker ps
error during connect: Get "http://%2F%2F.%2Fpi //./pipe/dockerDesktopLinuxEngine:

$ docker images
error during connect: Head "http://%2F%2F.%2FprDesktopLinuxEngine: Le fichier spécifié est introuvable



![Vérification Docker](chemin/vers/votre/capture/verification_docker.png)

> ⚠️ **Note** : Si vous rencontrez des erreurs, assurez-vous que Docker Desktop est en cours d'exécution.

## Récupération de l'image Docker

Récupérez l'image "welcome-to-docker" avec la commande :

docker pull docker/welcome-to-docker

$ docker pull docker/welcome-to-docker
Using default tag: latest
error during connect: Post "http://%2F%2F.%2Fpge=docker%2Fwelcome-to-docker&tag=latest": opest introuvable.


![Pull Image](chemin/vers/votre/capture/pull_image.png)

## Construction et exécution du conteneur

Lancez le conteneur avec la commande :

docker run -it --rm -p 8080:80 docker/welcome-to-docker



Accédez à `http://localhost:8080` dans votre navigateur.

![Run Container](chemin/vers/votre/capture/run_container.png)

## Arrêt et suppression du conteneur

Pour arrêter le conteneur, utilisez `Ctrl+C` dans le terminal ou exécutez :

docker stop $(docker ps -q --filter ancestor=docker/welcome-to-docker)



![Stop Container](chemin/vers/votre/capture/stop_container.png)

## Suppression de l'image

Supprimez l'image avec :

