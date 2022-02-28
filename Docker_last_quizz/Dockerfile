# Image Service base de données Redis basé sur une image redis (version officielle Docker : https://hub.docker.com/_/redis)

FROM redis
COPY redis.conf .
CMD [ "redis-server", "." ]

# 0 docker pull redis
# (1. Build image redis redis_service : " docker build -t service_redis . ) !!! non, faire précédent !!!
# 2. Docker-Compose avec image dockerfacile/app qui a une dépendance a image redis_service, puis : " docker-compose up ""