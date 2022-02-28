# Virtualization

## Table of Contents

- [Virtualization](#virtualization)
  - [Table of Contents](#table-of-contents)
  - [Micro Services Architecture](#micro-services-architecture)
  - [Tools](#tools)
  - [What is Docker](#what-is-docker)
  - [Docker setup](#docker-setup)
  - [Useful COmmands](#useful-commands)
  - [Docker APIs](#docker-apis)
  - [Docker Images](#docker-images)
  - [Benefits of Docker](#benefits-of-docker)
  - [Differences between Docker and Virtualization](#differences-between-docker-and-virtualization)
  - [Monolith vs Micro-services](#monolith-vs-micro-services)

## Micro Services Architecture

## Tools

## What is Docker

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

## Docker APIs

## Docker Images

## Benefits of Docker

## Differences between Docker and Virtualization

## Monolith vs Micro-services
