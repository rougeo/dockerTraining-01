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
- Lister les images
```
$ docker images
```
- Recuperer une  images
```
$ docker pull nom_image:tag_image
```

-  Demarrer un container docker
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

## Creation des images docker.
Les images docker sont créées avec un fichier appélé Dockerfile
```
FROM debian:12.5

RUN apt-get update && apt-get install -y python3


```
-  Construction de l'image
```
$ docker build -t nom_image:tag_image .
```
# References
- https://docs.docker.com/engine/install/ubuntu/
