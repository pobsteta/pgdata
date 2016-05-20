Docker notes
============

Enregistrer une image
---------------------

docker commit <ID> pgdata_bef

Taguer une image
----------------

docker tag <ID> pobsteta/pgdata:bef

Utiliser le dépôt docker
------------------------

Se logguer au serveur docker et pousser l'image sur le serveur.

```sh
sudo docker login
sudo docker push pobsteta/pgdata:latest
```

Recevoir l'image du serveur docker :

```sh
sudo docker pull pobsteta/pgdata
```

Utiliser Trusted Build
----------------------

Pour automatiser les builds successifs, renseigner sur le serveur docker Trusted Builds

Chaque commit réalisé sur le dépôt GitHub réalisera un build automatiquement sur le serveur Docker.
Cette nouvelle version sera tagguée pobsteta/pgdata:tag, en remplaçant tag par latest ou full ou bef

Pour plus d'informations sur Trusted Build : http://docs.docker.io/docker-io/builds/
