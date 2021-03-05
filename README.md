## Prérequis
Pour lancer ce projet vous devez d'abord installer docker sur votre machine.
Allez sur ce [lien](https://docs.docker.com/get-docker/) et telechargez puis installez la version docker qui vous concerne.

## Présentation

Ces conteneurs ont été initialement issus de https://github.com/liliasfaxi/hadoop-cluster-docker

J'ai créé un nouveau conteneur qui lance le hadoop automatiquement au demarage.
Vous pouvez le telecharger directement dans le docker hub avec la commande `docker pull genieouz/hadoop-setup:1.0`

## Fonctionnalités

Ce projet lance un cluster de 3 machines 1 master et 2 slaves dont chacun se trouve dans un conteneur docker.
Vous pouvez utiliser l'image `genieouz/hadoop-setup:1.0` qui se trouve dans le docker hub pour lancer un seul conteneur(le master) contenant les configurations nécessaires.
Utilisez la commande suivante dans ce cas `docker run -itd -p 50070:50070 -p 8088:8088 -p 7077:7077 -p 16010:16010 --name hadoop-master --hostname hadoop-master genieouz/hadoop-setup:1.0`
et acceder à l'interface hadoop via [http://localhost:50070/](http://localhost:50070/). 

## Lancement du cluster

Pour lancer le cluster avec le master et les deux slaves, utilisez la commande suivante
`docker-compose up -d`
puis acceder à l'interface de hadoop via [http://localhost:50070/](http://localhost:50070/)