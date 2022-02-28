# Image sur laquelle se baser
FROM openclassrooms/build_image

# Image equipé d'un serveur nginx : Installer serveur nginx
RUN apt-get update \
    && apt-get -y install \
        nginx

# Le démarrer (NON, pas besoin de le lancer)
#CMD ["nginx", "-g", "daemon off;"]

# Build image : " docker build -t oc_tp . "
# Run image : " docker run -it oc_tp "
