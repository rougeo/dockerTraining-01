# Docker Tuto

## Installation

### Script
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```
### Validation de l'Installation
````
$ sudo docker version
````

### Ajouter l'utilisateur dans le groupe docker
```
$ sudo usermod -aG docker $USER
```
Après ajout de l'utilisateur on redemare la machine

## Commandes de base de docker
*Lister les images
```
$ docker images
```
*Recuperer une  images
```
$ docker pull nom_image:tag_image
```

* Demarrer un container docker
```
$ docker run --name container_name -it nom_image:tag_image {CMD- optionnelle}
```

-  Lister les   containers docker en exécution
```
$ docker ps
```
-  Lister tous les   containers docker (running and stopped)

```
$ docker ps -a
```

- Supprimer un container
```
$ docker rm container_id___OR__container_name
```
* Accèder à un container en shell
```
$ docker exec -it container_id__OR__container_name sh
```

## Creation des images docker.
Les images docker sont créées avec un fichier appélé Dockerfile
```
FROM debian:12.5

RUN apt-get update && apt-get install -y python3


```
  Construction de l'image
```
$ docker build -t nom_image:tag_image .
```

## Docker Compose
### Installation
Docker compose est dejà installé en tant que plugin docker
### Exemple
```
version: "3.9"
services:
  site-1:
    image: ubuntu/apache2:2.4-21.10_edge
    container_name: test2
    ports:
      - 8086:80
```
### Commandes de bases
* Demarrer les services
```
$ docker compose up -d
```

# Apache2 
## Installation
```
$ sudo apt-get update
$ sudo apt-get install apache2
```
## Valider l'Installation

```
$ sudo service apache2 status
```


# References
* https://docs.docker.com/engine/install/ubuntu/
* https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-20-04
