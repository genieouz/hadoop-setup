## Présentation

Ces contenaires ont été initialement issus de https://github.com/liliasfaxi/hadoop-cluster-docker

J'ai créé un nouveau conteneur qui lance le hadoop automatiquement au demarage du conteneur.
Vous trouverez ce conteneur dans le docker hub 
### genieouz/hadoop-setup

## Fonctionnalités

Ce projet lance un cluster de 3 machines 1 master et 2 slaves dont chacun se trouve dans un conteneur.
Vous pouvez utilisez l'image genieouz/hadoop-setup qui se trouve dans le docker hub pour lancer un seul conteneur 
contenant la configuration de hadoop et acceder à l'interface de hadoop via [http://localhost:50070/](http://localhost:50070/)

## Lancement du cluster

Pour lancer le cluster avec le master et les deux slaves, utilisez la commande suivante
`docker-compose up -d`
puis acceder à l'interface de hadoop via [http://localhost:50070/](http://localhost:50070/)