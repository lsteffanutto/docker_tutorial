### Conteneur 0 test

# Télécharge une image de base pour notre conteneur

#FROM alpine:3.14 

# Indiquer une commande à effectuer avec le conteneur
# Imprime sur sortie standard "Hello World !"

#CMD ["echo", "Hello World !"]

# Ce conteneur va donc télécharger l'image puis print le message
# Quand le dockerfile est écrit il faut construire notre image
# docker build -t mon_image .
# = construire mon image avec le nom "mon_image" dans le dossier de référence .

###

# FROm utilisable qu'une fois dans un Dockerfile, permet de choisir image à utiliser comme base (ici image de base Debian 9)
FROM debian:9

# RUN = executer une commande dans le conteneur 
RUN apt-get update -yq \
&& apt-get install curl gnupg -yq \
&& curl -sL https://deb.nodesource.com/setup_10.x | bash \
&& apt-get install nodejs -yq \
&& apt-get clean -y

# Ajouter les sources de notre application locale dans le dossier /app/
ADD . /app/

# " CD app "
WORKDIR /app

# installer le package du projet Node.js
RUN npm install

# corriger avec ça : https://openclassrooms.com/forum/sujet/docker-creer-son-dockerfile

ADD . /app/

# MTNT code source et dépendances bien présents dans conteneur.

# EXPOSE : indiquer le port sur lequel l'application écoute
EXPOSE 2368
# VOLUME : indiquer quel répertoire partager avec notre host
VOLUME /app/logs

# Ces deux derniers pas nécessaire au fonctionnement de notre image Docker

# Dernière ligne : instruction qui doit tjrs être présente
# Permet ua conteneur de savoir quelle commande il doit exécuter lors de son démarrage

CMD npm run start