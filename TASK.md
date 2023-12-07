# <div align="center">**DOCKER LEARNING HANDBOOK**</div>
# Table of Contents

- **[What is Docker?](#what-is-docker)**
- **[Why Use Docker?](#why-use-docker)**
- **[How does Docker work?](#how-does-docker-work)**
- **[Installing Docker](#installation)**
- **[Common Commands](#common-docker-commands)**
- **[Dockerfile](#dockerfile)**
- **[Network Commands](#3-network-commands)**
- **[Volume Commands](#4-volume-commands)**
- **[Docker Compose Commands](#5-docker-compose-commands)**
- **[Docker Swarm](#6-docker-swarm)**

### What is Docker?
Docker is an open-source platform that automates the deployment, scaling, and management of applications within lightweight, portable containers. Containers encapsulate an application and its dependencies, ensuring consistent and reliable execution across various environments.

### Why use Docker?

1. **Consistency:** Docker ensures consistency in development, testing, and production environments, reducing the "it works on my machine" problem.
2. **Isolation:** Containers encapsulate applications, preventing conflicts between dependencies and ensuring a clean runtime environment.
3. **Portability:** Docker containers run consistently across different machines and platforms, simplifying application deployment.

### How Does Docker Work?

Docker utilizes containerization technology, allowing applications to run in isolated environments called containers. Containers share the host OS kernel but have their own file system, processes, and network interfaces. Docker images contain everything needed to run an application, making it easy to deploy and scale.


---

## Installation

To begin your Docker journey, install Docker on your machine using the following steps:

### Linux


sudo apt update
sudo apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker

### macOS

#### Install Docker Desktop
1. [Download Docker Desktop](https://docs.docker.com/desktop/install/mac/).
2. Follow the installation instructions provided for macOS.

### Windows

#### Install Docker Desktop
1. [Download Docker Desktop](https://docs.docker.com/desktop/install/windows/).
2. Follow the installation instructions provided for Windows.


##  Common Docker Commands 

### 1. Basic Commands 

#### Check Docker Version
```bash
docker --version
```
#### Display System-wide Docker Information
```bash
docker info
```
#### Create and Start a Container from an Image
```bash
docker run <image>
```
#### List Running Containers
```bash
docker ps
```

#### List All Containers (Including Stopped Ones)
```bash
docker ps -a
```

#### Stop a Running Container
```bash
docker stop <container>
```

#### Remove a Stopped Container
```bash
docker rm <container>
```

### 2. Image Commands
#### List Available Images
```bash
docker images
```

#### Download an Image from Docker Hub
```bash
docker pull <image>
```

#### Remove an Image
```bash
docker rmi <image>
```

### 3. Container Lifecycle

#### Start a Stopped Container
```bash
docker start <container>
```

#### Restart a Container
```bash
docker restart <container>
```

#### Pause a Running Container
```bash
docker pause <container>
```

#### Unpause a Paused Container
```bash
docker unpause <container>
```

### Dockerfile
A Dockerfile is a script that defines the steps to build a Docker image. Here's a simple example for a Python application:

#### 1.Use an official Python runtime as a parent image
FROM python:3.8-slim

#### 2.Set the working directory in the container
WORKDIR /app

#### 3.Copy the current directory contents into the container at /app
COPY . /app

#### 4.Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

#### 5.Make port 80 available to the world outside this container
EXPOSE 80

#### 6.Define environment variable
ENV NAME World

#### 7.Run app.py when the container launches
CMD ["python", "app.py"]


### 3. Network Commands

#### List Docker Networks
```bash
docker network ls
```

#### Create a Docker Network
```bash
docker network create <network>
```

#### Display Detailed Network Information
```bash
docker network inspect <network>
```

### 4. Volume Commands
##### List Docker Volumes
```bash
docker volume ls
```


#### Create a Docker Volume
```bash
docker volume create <volume>
```

#### Display Detailed Volume Information
```bash
docker volume inspect <volume>
```

### 5. Docker Compose Commands
#### Create and Start Containers Defined in docker-compose.yml
```bash
docker-compose up
```

#### Stop and Remove Containers
```bash

docker-compose down
```
#### List Services and Their Status
```bash
docker-compose ps
```

#### View Output from Containers
```bash
docker-compose logs
```

### 6. Docker Swarm

Docker Swarm is Docker's native clustering and orchestration solution for managing multiple containers across a cluster of machines.

#### Concepts

- **Node:** A machine (physical or virtual) running Docker, which participates in the swarm.
- **Service:** A definition of a task to execute in the swarm.
- **Task:** The smallest deployable unit in a swarm, representing a container.

#### Commands

- `docker swarm init`: Initialize a swarm.
- `docker swarm join`: Join a node to the swarm.
- `docker node ls`: List nodes in the swarm.
- `docker service create`: Create a new service.
- `docker service ls`: List services in the swarm.
- `docker service ps <service>`: List tasks in a service.

Note: Replace <image>, <container>, <network>, and <volume> with actual names or IDs in the commands.

