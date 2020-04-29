# FormationPython

Les exercices se trouvent dans le dossier python.

##Python
fichier LessonOneHitema

##Datavisualisation
fichiers LessonDataViz1, LessonDataViz2, LessonDataViz3, LessonDataViz4, LessonDataVizKPI3

##Docker
fichier Dockerfile à la racine du git


##réponses : 
1. sudo groupadd docker
2. sudo gpasswd -a $USER docker

Par défaut le démon docker doit toujours être lancé en root, ou avec sudo devant. Mais depuis la version 0.5.2, si un user fait parti du groupe docker, alors Unix va le considérer comme équivalent a root.


Cheatsheet : 
docker info : affiche les infos systeme
Docker pull : télécharger une image
docker push : Publier une image
docker pull:sid : télécharger avec sid
docker run -ti debian:laster bash : exécute la plus récente image de debian

docker build xx : creer image

docker images -a : liste toutes les images
docker images -q : liste les id des images
docker container ls -a (==docker ps -a): liste container créés
docker container ls : liste containers actifs
docker commit idContainer nomContainer

docker rmi idImage : supprime image
docker rmi $(docker images -q) : supprime toutes les images

docker rm idContainer : supprime le container
docker rm $(docker ps -a -q) : supprime tous les containers
docker commit container_id image_name : applique les changements d un container a une image

docker network ls : affiche les réseaux par defaut
docker cp : copie fichiers/dossier depuis le PATH d'un container vers le HOSTDIR
docker diff : inspecter les changements
docker exec : executer une commande dans un container en cours d'éxécution
docker exec -it idContainer bash : entrer dans le terminal du dock

docker kill : tue un container en cours d'éxécution
docker login : connexion au docker hub