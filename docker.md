# Docker commands

## Auth

```markdown
docker login
docker logout
```

## Manipulating images & containers

```markdown
# RUN IMAGE (with default command)
docker run -d -p [local port]:[container port] [image] [?custom command]
docker run redis
docker run busybox ls
docker run -p 8080:8080 webserver
#   -p  port mapping
#   -d  detached mode

# VULUMES 
docker run -v /path/in/container -v /path/in/local:/path/in/container webserver
#   -v /path/in/container - this dir isn't be mapped
#   -v /path/in/local:/path/in/container - map local directory => container directory

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

# Step. Base image
FROM alpine

# On each step of building process:
#    1. a temporary container is created from prev. step
#    2. given command is executed on that container
#    3. a new image is created from that container

# Step. Execute a command on intermediate container
RUN apk add --update redis

# Step. Change working directory in container
WORKDIR usr/app

# Step. Copy some files from building directory to container
COPY ./ ./

# Step. Set primary command to be executed when container is started
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

# Docker compose

```
# Start docker containers from "docker-compose.yml"
docker-compose up
docker-compose up -d
docker-compose up --build
#   -d -detached mode
#   --build rebuild containers

# Stop all containers
docker-compose down
```

```yaml
# docker-compose.yml

# Specify version of docker compose
version: '3'

# Same network is generated for all services
# Name of service is it's hostname (redis-server, node-app)
# Container can be built from current Dockerfile
services:
    redis-server:
        image: 'redis'

    node-app:
        restart: 'no' | always | on-failure | unless-stopped
        build: .
        ports:
            - "8081:8081"
```

# Kubernetes
[Free kubernetes hosting](https://medium.com/techprimers/free-tiers-in-different-cloud-platforms-for-trying-out-kubernetes-2ccda3f296dc#id_token=eyJhbGciOiJSUzI1NiIsImtpZCI6IjE3MTllYjk1N2Y2OTU2YjU4MThjMTk2OGZmMTZkZmY3NzRlNzA4ZGUiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJodHRwczovL2FjY291bnRzLmdvb2dsZS5jb20iLCJuYmYiOjE2MjI0NzExOTEsImF1ZCI6IjIxNjI5NjAzNTgzNC1rMWs2cWUwNjBzMnRwMmEyamFtNGxqZGNtczAwc3R0Zy5hcHBzLmdvb2dsZXVzZXJjb250ZW50LmNvbSIsInN1YiI6IjExODE1ODQwMDA0NDA5NjU1NjcyOCIsImVtYWlsIjoidnR1bWFub3Y3ODJAZ21haWwuY29tIiwiZW1haWxfdmVyaWZpZWQiOnRydWUsImF6cCI6IjIxNjI5NjAzNTgzNC1rMWs2cWUwNjBzMnRwMmEyamFtNGxqZGNtczAwc3R0Zy5hcHBzLmdvb2dsZXVzZXJjb250ZW50LmNvbSIsIm5hbWUiOiJWYWxlcml5IiwicGljdHVyZSI6Imh0dHBzOi8vbGgzLmdvb2dsZXVzZXJjb250ZW50LmNvbS9hLS9BT2gxNEdpb2p6ZklxRUdNWlR0YXQ5ejV0YkN0VkRCV0F1MTN0S0FoWFdaTTZBPXM5Ni1jIiwiZ2l2ZW5fbmFtZSI6IlZhbGVyaXkiLCJpYXQiOjE2MjI0NzE0OTEsImV4cCI6MTYyMjQ3NTA5MSwianRpIjoiNWU1ZTBkZDM1ZTk3NGMzMGVjZjY2NWQ0MTI1YWE1MmRhNWRiMTQ1NSJ9.fpJzhap9EEWzSK1DKTOuZLzK1K32zlLANZGtJ1AZNPqX0_roSRfItDLFVyTi5asCWvXZvLquaydJ2o3Pnm2dVmsSQuDe2IsQ_kHP_QNzdEfzqtoADAbsiuDuAAYaItQvKK7QAHAbOobnuOGFQwhdhbJ76-_35naQxEsf1n85JQnZjj1ocr5HF3SO1Hdn4wTUxpI6PKoEYNlfnu63w9ju6gmqCcYvNFJl-9HGUXgEFJKKOQFLP9n9VeZW3yzbs1EChWTKgYFFrCLXqwlAIdl5l0LQt5C5EBn0ou5xpnvFpiXrRE5YtVdNTD76bdqBHdDJMAJPsZuhVWYkOtilQT5m1A)

[install minikube](https://kubernetes.io/ru/docs/tasks/tools/install-minikube/)

```yaml
# client-pod.yaml

apiVersion: v1
kind: Pod
metadata:
  name: client-pod
  labels:
    component: web
spec:
  containers:
    - name: client
      image: stephengrider/multi-client
      ports:
        - containerPort: 3000
```

```yaml
# client-node-port.yaml

apiVersion: v1
kind: Service
metadata:
  name: client-node-port
spec:
  type: NodePort
  ports:
    - ports: 3050
      targetPort: 3000
      nodePort: 31515
  selector:
    component: web
```
![Objects](https://i.imgur.com/UUP5mWY.png)
![NodePort Mapping](https://i.imgur.com/cdVu59j.png)
![Port Mapping](https://i.imgur.com/5SONIwD.png)
![Important takeaways](https://i.imgur.com/aiMw6ru.png)

```
# applying kubectl configuration changes

kubectl apply -f client-pod.yaml
kubectl apply -f client-node-port.yaml

# get the status of pods
kubectl get pods
# get the status of services
kubectl get services
# get information about object
kubectl describe <object type> <object name>
```

```
# get the ip of minikube VM
minikube ip
```
