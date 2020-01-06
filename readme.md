[![CircleCI](https://circleci.com/gh/YI-B3-Devops/tp2-team-11/tree/master.svg?style=svg)](https://circleci.com/gh/YI-B3-Devops/tp2-team-11/tree/master)

# B3 Devops - Projet 1
- [Info](#info)
- [Team 11](#team-11)
  * [Les fichiers du repo](#les-fichiers-du-repo)
  * [Pré-requis](#pré-requis)
- [Installation](#installation)
- [Utilisation de l'API](#utilisation)
- [Fermer le projet](#fermer-le-projet)

## Info

### Team 11

* mail: zakarya.tolba@ynov.com  <br>
github_username: zaktolba <br>

* mail: nicolas.laroche@ynov.com<br>
github_username: laroche-nicolas<br>

* mail: nicolas.notararigo@ynov.com<br>
github_username: Neerfix<br>


### DockerHub
link: https://hub.docker.com/repository/docker/neerfix/tp2-team-11

### DockerHub
Basé sur le projet : https://github.com/YI-B3-Devops/tp2-notararigo-nicolas

### Les fichiers du repo

- Readme (ce fichier)
- [ChangeLog](./changelog.md) - _Changements effectués au long des releases_ 
- [package.json](./package.json) - Fichier de NPM.
- .cicleci
    - [config.yml](./.circleci/config.yml) - Fichier de configuration de circleci
- [docker](./docker/) - Contient les containers docker.
    - [docker-compose](./docker/docker-compose.yml) - docker compose du projet.
        - [api](docker/api/Dockerfile) - Dockerfile de NodeJs.
        - [nginx](./docker/nginx/Dockerfile) - Dockerfile de Nginx.
            - [nginx.conf](./docker/nginx/nginx.conf) - configuration de Nginx.   

### Pré-requis
* Docker
* Node.js

## Installation

1) Clôner le repo dans votre espace. 
2) Se rendre dans le dossier avec son terminal.
3) Lancer ```npm install``` afin d'installer les modules de Node
4) Lancer la commande suivante pour se rendre dans le dossier de docker et lancer le projet : 
```bash 
cd docker && docker-compose up
```

Vous pouvez vous rendre sur le serveur via 
[localhost:8080](http://localhost:8080)

## Utilisation
- GET /

```
Welcome on Nginx
```
- GET /api
```
{"message": "Hello World" }
```
- GET /status
```
{"status": "OK", "postgresUptime": String, "redisConnectedClients": Number}
```

## Fermer le projet 
1) Se rendre dans le dossier avec son terminal
2) Lancer la commande suivante pour se rendre dans le dossier de docker et arrêter le projet : 
```bash 
cd docker && docker-compose down
```
