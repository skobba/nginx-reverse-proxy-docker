# nginx-reverse-proxy-docker

# Ref
https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion.git

# Run
docker-compose up -d

# Expose on localhost
docker run -p 8080:8080 jboss/keycloak

# Container Shell
docker exec -it d06c64f5607b sh
docker exec -it nextcloud_app_1 sh
docker exec -it nextcloud_letsencrypt-companion_1 sh
docker exec -it nextcloud_proxy_1 sh



# Creating admin account
docker run -e KEYCLOAK_USER=keycloak -e KEYCLOAK_PASSWORD=keycloak jboss/keycloak

# Create an account on an already running container by running:
docker exec be1ed8c4e8c4 keycloak/bin/add-user-keycloak.sh -u admin -p keycloak


docker restart be1ed8c4e8c4

# Remove containers
docker-compose rm
