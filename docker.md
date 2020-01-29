# Docker commands

## Auth

```markdown
docker login
docker logout
```

## Manipulating images & containers

```markdown
# RUN IMAGE (with default command)
docker run [image] [?custom command]
docker run redis
docker run busybox ls


# run = create + start
docker create hello-world [?custom command]
docker start [-a] [container_id]
#       -a    -attach process.STDOUT => terminal

# SHOW RUNNING CONTAINERS
docker ps

# ...including stopped
docker ps --all

# SHOW OUTPUT of a container
docker logs [container_id]

# EXECUTING COMMANDS in running containers
docker exec [-it] [container_id] [command]
docker exec -it ecb344342 redic-cli
#       -i    -attach terminal => process.STDIN
#       -t    -nice formatting

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

## Building custom images

1. Create a Dockerfile:

```markdown
# Dockerfile

# Step 1. Base image
FROM alpine

# On each step of building process:
#    1. a temporary container is created from prev. step
#    2. given command is executed on that container
#    3. a new image is created from that container

# Step 2. Execute a command on intermediate container
RUN apk add --update redis

# Step 3. Set primary command to be executed when container is started
CMD ["redis-server"]
```

2. Build an image

```markdown
docker build [-t image name] .
docker build .
docker build augustbright/redis-server:latest
#   -t  -tag (convention: [user name]/[image name]:[tag])

# COMMIT container changes to make a new image
#(...interesting but bad approach)
docker commit -c 'new commands' [container_id]
docker commit -c 'CMD["redis-server"]' [container_id]
```
