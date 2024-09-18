# Docker-Container-MariaDB

### Create easily containers with MariaDB and phpMyAdmin ready to go

## Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

_Docker Compose should be included when you install Docker on your computer, if not, you can download it separately from the official documentation: https://docs.docker.com/compose/install/_

## How to use

All you need to do is to run this command:

```bash
docker compose up -d
```
_Note: If the `docker compose` command is not found, try `docker-compose` instead_


The mariadb and phpmyadmin containers will be started automatically.

Now that the containers are running, you can access phpMyAdmin using the following link:

- [phpMyAdmin](http://localhost:8080)

## How to stop

If you want to stop the containers, you can run this command in the same directory of the docker-compose file:

```bash
docker compose down
```

By default, the containers will not stop until you stop it yourself, even after the machine is shut down and restarted they will still be running or start automatically.

You can delete this line in both the mariadb and phpmyadmin configs to avoid this behavior:

```yaml
restart: unless-stopped
```

And after that, remember to run the docker-compose file again to update the configuration.

## Useful Commands

_Note: If the `docker compose` command is not found, try `docker-compose` instead_

- `docker compose up -d`: Start the containers / update existing containers
- `docker compose down`: Stop the containers
- `docker compose restart`: Restart the containers
- `docker ps`: Check active containers
- `docker ps -a`: Check all containers
- `docker rm 'CONTAINER_NAME'`: Remove a container with the name 'CONTAINER_NAME'
- `docker images`: Check all images
- `docker rmi 'IMAGE_NAME'`: Remove an image with the name 'IMAGE_NAME'
- `docker volume ls`: Check all volumes
- `docker volume rm 'VOLUME_NAME'`: Remove a volume with the name 'VOLUME_NAME'
- `docker volume create 'VOLUME_NAME'`: Create a new volume with the name 'VOLUME_NAME'
- `docker exec -it 'CONTAINER_NAME' bash`: Execute a bash shell in the container with the name 'CONTAINER_NAME'

## Useful Links

- [Docker Compose](https://docs.docker.com/compose/)
- [Docker](https://www.docker.com/)
- [Docker Hub](https://hub.docker.com/)

