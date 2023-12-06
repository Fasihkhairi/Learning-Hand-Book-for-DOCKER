# Docker Learning Handbook



### What is Docker?

Docker is an open-source platform that automates the deployment, scaling, and management of applications within lightweight, portable containers. Containers encapsulate an application and its dependencies, ensuring consistent and reliable execution across various environments.

### Why Docker?

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

# Common Docker Commands

## Basic Commands

### Check Docker Version


docker --version
