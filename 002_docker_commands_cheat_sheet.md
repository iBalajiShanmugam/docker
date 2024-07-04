```markdown
# Docker Commands Cheat Sheet

## Creating and Running a container from an image

```bash
docker run hello-world
```

## Overriding default command

```bash
docker run busybox echo "hi there"
docker run busybox ls
docker run busybox pwd
```

## Listing Running containers

```bash
docker ps             # Lists active containers
docker ps -a          # Lists all containers (including inactive)
```

## Container Lifecycle

```bash
docker run <image>    # Creates and starts a container
docker create <image> # Creates a container
docker start <container_id>  # Starts a created container
docker start -a <container_id>  # Starts and attaches to a container
```

## Restarting stopped container

```bash
docker start <container_id>
docker start -a <container_id>
```

## Removing stopped container

```bash
docker system prune   # Remove all stopped containers
docker rm <container_id>
```

## Retrieving logs

```bash
docker logs <container_id>
```

## Stopping container

```bash
docker create busybox ping google.com
docker start <container_id>
docker stop <container_id>   # Gracefully stop container (default 10 seconds)
docker kill <container_id>   # Forcefully stop container
```

## Multicommand container

```bash
docker run redis
docker exec -it <container_id> redis-cli   # Execute interactive command in running container
docker exec <container_id> sh             # Execute command in running container
```

## Starting with shell (-it for interactive mode)

```bash
docker run -it busybox sh
```

## Container isolation

```
Docker containers are isolated from each other and the host system, providing a controlled environment for applications.
```

This cheat sheet covers essential Docker commands for managing containers. Replace `<container_id>` with the actual container ID obtained from `docker ps` or `docker ps -a` commands.
```
