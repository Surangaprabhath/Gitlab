# Gitlab
Gitlab deployment using docker compose

# Create a self sign certificate
mkdir -p gitlab/ssl

openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
  -keyout gitlab/ssl/gitlab.example.com.key \
  -out gitlab/ssl/gitlab.example.com.crt \
  -subj "/CN=gitlab.example.com"

# Prepare Docker Compose file

vi docker-compose.yml

adjust the docker-compose.yml file as your requirements

# Up the docker compose 
docker-compose up -d

verify the URL
https://gitlab.example.com
