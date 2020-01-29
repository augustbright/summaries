# Docker commands

## Auth

```
docker login
docker logout
```

## MAnipulating images & containers

```
# RUN IMAGE (with default command)
docker run [image] [?custom command]
docker run redis
docker run busybox ls


# run = create + start
docker create hello-world [?custom command]
docker start [-a] [container_id]
    # -a    -attach process.STDOUT => terminal

# SHOW RUNNING CONTAINERS
docker ps

# ...including stopped
docker ps --all

# SHOW OUTPUT of a container
docker logs [container_id]

# EXECUTING COMMANDS in running containers
docker exec [-it] [container_id] [command]
docker exec -it ecb344342 redic-cli
    # -i    -attach terminal => process.STDIN
    # -t    -nice formatting

# ...or start a shell in container (ctrl+d to exit or type "exit"):
docker exec [-it] [container_id] sh # ...or bash

# ...or run an image with a shell
docker run -it busybox sh

# STOP CONTAINER (SIGTERM)
docker stop [container_id]

# ...or, but better not use it (SIGKILL)
docker kill [container_id]

# DELETE STOPPED CONTAINERS and other clean up
docker system prune

```
