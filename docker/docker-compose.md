# Docker Compose: Multi-container Docker Applications

Docker Compose is a tool for defining and managing multi-container Docker applications. With Compose, you can use a YAML file to configure application services, networks, and volumes, simplifying the process of running multi-container applications seamlessly.

Project Homepage: [Docker Compose: Define and run multi-container applications with Docker](https://docs.docker.com/compose/)
Documentation: [Docker Compose Overview](https://docs.docker.com/compose/overview/)

---

## Docker compose CLI

**Run Containers**

COMMAND | DESCRIPTION
---|---
`docker-compose up` | Start services as defined in the `docker-compose.yml` file.
`docker-compose up -d` | Start services in detached mode, running in the background.
`docker-compose down` | Stop and remove all the services defined in the `docker-compose.yml` file.
`docker-compose restart` | Restart services.
`docker-compose start [service-name]` | Start a specific service.
`docker-compose stop [service-name]` | Stop a specific service.
`docker-compose ps` | List containers and their status.
`docker-compose logs [service-name]` | View logs of a specific service.
`docker-compose run [service-name] [command]` | Run a one-off command for a specific service.
`docker-compose exec [service-name] [command]` | Execute a command in a running container of a specific service.

## Networking
By default Docker-Compose will create a new network for the given compose file. You can change the behavior by defining custom networks in your compose file.
### Create and assign custom network
*Example:*
```yaml
networks:
  custom-network:

services:
  app:
    networks:
      - custom-network
```
### Use existing networks
If you want to use an existing Docker network for your compose files, you can add the `external: true` parameter in your compose file
*Example:*
```yaml
networks:
  existing-network:
    external: true
```

## Volumes
Volumes allow Docker containers to use persistent storage. In a compose file, you can create and map volumes like this:
```yaml
volumes:
  my-volume:

services:
  app:
    volumes:
      - my-volume:/path-in-container
```

These volumes are stored in `/var/lib/docker/volumes`.
