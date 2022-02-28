# Depuis la doc officielle de Docker pour Python : https://hub.docker.com/_/python
# Permet de créer une image du code en Python : install les dépendance et exécute le main

FROM python:3

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./main.py" ]



### CORRECTION OPENCLASSROOM ###
# base image
# FROM python:3.8-alpine3.14

# # copy just the requirements.txt first to leverage Docker cache
# # install all dependencies for Python app (va chercher les requirements dans le dossier où ils se trouvent)
# COPY ./requirements.txt /app/requirements.txt

# Se déplace dans le dossier de l'app 'dans le cas où on range les fichiers proprement'
# WORKDIR /app

# # install dependencies in requirements.txt
# RUN pip install -r requirements.txt

# # copy all content to work directory /app
# COPY . /app

# # specify the port number the container should expose (!!! Dans mon cas ne marchait pas pour premier exo!!!)
# EXPOSE 5000

# # run the application
# CMD ["python", "/app/main.py"]