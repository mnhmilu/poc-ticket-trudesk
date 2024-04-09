# poc-ticket-trudesk

ticketing system 



## Troubleshoot

Volume not persisting when using `sudo docker-compose restart`

check

```groups nahid
less /etc/passwd```

add this

`sudo usermod -aG docker $USER`


## References

[Trudesk Documentation](https://docs.trudesk.io/v1.2/getting-started/deployment/docker-deployment)

```
Docker Compose is a tool for defining and running multi-container Docker applications. It uses YAML files to configure the application's services, networks, and volumes. Below are the most commonly used commands in Docker Compose and when you might want to use each:

docker-compose up:

When to use: Use this command to start up your Docker containers defined in the docker-compose.yml file.
Example: docker-compose up
docker-compose down:

When to use: This command stops and removes containers, networks, volumes, and images created by docker-compose up.
Example: docker-compose down
docker-compose build:

When to use: Use this command to build or rebuild services defined in the docker-compose.yml file.
Example: docker-compose build
docker-compose start:

When to use: This command starts services that were defined in the docker-compose.yml file but are currently stopped.
Example: docker-compose start
docker-compose stop:

When to use: Stop services defined in the docker-compose.yml file, but don't remove containers, networks, volumes, or images.
Example: docker-compose stop
docker-compose restart:

When to use: Restart services defined in the docker-compose.yml file.
Example: docker-compose restart
docker-compose pause:

When to use: Pause services defined in the docker-compose.yml file.
Example: docker-compose pause
docker-compose unpause:

When to use: Unpause services defined in the docker-compose.yml file.
Example: docker-compose unpause
docker-compose logs:

When to use: View output from containers started by docker-compose up.
Example: docker-compose logs
docker-compose ps:

When to use: List containers started by docker-compose up.
Example: docker-compose ps
docker-compose exec:

When to use: Execute a command in a running container.
Example: docker-compose exec service_name command
docker-compose run:

When to use: Run a one-off command on a service.
Example: docker-compose run service_name command
These are the primary commands you'll use with Docker Compose for managing your multi-container applications. The commands offer a range of functionality from starting and stopping services to viewing logs and executing commands within containers.
```
