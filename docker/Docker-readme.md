# Microservices

![docker architecture](./assets/images/docker-architecture.png)

## Table of Contents

- [Microservices](#microservices)
  - [Table of Contents](#table-of-contents)
  - [Micro Services Architecture](#micro-services-architecture)
  - [Tools](#tools)
  - [What is Docker](#what-is-docker)
  - [Docker setup](#docker-setup)
  - [Useful COmmands](#useful-commands)
  - [Benefits of Docker](#benefits-of-docker)
  - [Hosting static website with Nginx and Docker](#hosting-static-website-with-nginx-and-docker)
  - [Docker compose folder structure](#docker-compose-folder-structure)
  - [Run docker compose](#run-docker-compose)

## Micro Services Architecture

## Tools

## What is Docker

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

## Docker setup

Install and setup Docker using [this link](https://docs.docker.com/desktop/windows/install/)

Check if Docker is installed using `docker version`.

In case we encounter the **TTY** do `alias docker="winpty docker"`

## Useful COmmands

- `docker pull`: pull a specific image
- `docker push`: push a specific image
- `docker run`: run a specific image
- `docker login`: adds your credentials
- `docker stop <container-name-or-id>` stops the container
- `docker images`: displays all images in your system
- `docker rmi <image-name> -f`: removes the image by name/id. The `-f` forces it
- `docker ps` shows running containers. Adding `-a` flag displays all containers used.
- `docker run -d -p <destination-PORT>:<initial-PORT> <image-name>` runs a container. `-d` runs it in background and gives us back the terminal.
- `docker exec -it <container-id> sh` to enter a container. You should see a `#` sign at the beginning of the line if it was successful. You can check using `uname -a`.
- `docker commit <image-id> <username>/<repo-name>:<tag-name>` to commit a new version to DockerHub. **You have to first create the repo on DockerHub**.
- `docker push <username>/<repo-name>:<tag-name>` to push the version from your local machine to DockerHub
- `docker build -t <username>/<repo-name> .`
- `docker cp <container-name>:<origin-path> <destination-path>` to copy files from docker container to localhost

## Benefits of Docker

- Consistent and Isolated Environment
- Cost-Effectiveness with Fast Deployment
- Mobility - Ability to run Anywhere
- Repeatability and Automation
- Test, Roll Back and Deploy
- Flexibility
- Collaboration, Modularity and Scaling

## Hosting static website with Nginx and Docker

- Copy index.html from localhost to default location of nginx (`/usr/share/nginx/html/`)

## Docker compose folder structure

```bash
root --- app --- app files
        |       |
        |        Dockerfile
        |
         mongod.conf
        |
         docker-compose.yml
```

## Run docker compose

- `docker-compose -f docker-compose.yml up --detach` (from you root folder) to run the docker-compose file. The `--detach` flag runs the container in the background.
