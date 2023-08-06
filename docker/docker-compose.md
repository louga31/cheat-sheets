# Docker Compose: Multi-container Docker Applications

Docker Compose is a tool for defining and managing multi-container Docker applications. With Compose, you can use a YAML file to configure application services, networks, and volumes, simplifying the process of running multi-container applications seamlessly.

Project Homepage: [Docker Compose: Define and run multi-container applications with Docker](https://docs.docker.com/compose/)
Documentation: [Docker Compose Overview](https://docs.docker.com/compose/overview/)

---

## Docker compose CLI

**Run Containers**

COMMAND | DESCRIPTION
---|---
`docker compose up` | Create and start services.
`docker compose up -d` | Start services in detached mode.
`docker compose down` | Stop and remove containers, networks, volumes, and images created by `up`.
`docker compose restart` | Restart services.
`docker compose start [service-name]` | Start specific or all services.
`docker compose stop [service-name]` | Stop specific or all services.
`docker compose pause [service-name]` | Pause services.
`docker compose unpause [service-name]` | Unpause services.
`docker compose ps` | List the status of services.
`docker compose logs [service-name]` | View the logs.
`docker compose run [service-name] [command]` | Run a one-off command.
`docker compose exec [service-name] [command]` | Execute a command inside a running container.
`docker compose top [service-name]` | Display the running processes.
`docker compose rm [service-name]` | Remove stopped service containers.

**Configuration**

COMMAND | DESCRIPTION
---|---
`docker compose config` | Validate and view the Compose configuration.
`docker compose pull [service-name]` | Pull service images.
`docker compose push [service-name]` | Push service images.
`docker compose build [service-name]` | Build or rebuild services.

**Networking and Volumes**

COMMAND | DESCRIPTION
---|---
`docker compose port [service-name] [private-port]` | Print the public port for a port binding.
`docker compose volume` | Manage volumes.

**Other Commands**

COMMAND | DESCRIPTION
---|---
`docker compose --version` | Show the Docker Compose version information.
`docker compose --help` | Get help on docker compose.


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
