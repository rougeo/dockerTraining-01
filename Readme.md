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
# References
- https://docs.docker.com/engine/install/ubuntu/
