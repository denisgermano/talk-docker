# Docker

Denis Germano @ Grupy-RP

Crave Food Systems

---

## A little of the history

+++

## Physical servers

@ul
- One service for each server
  - Apache
  - Nginx
  - Tomcat
  - MySQL
  - MongoDb
  - Microsoft IIS
@ulend

+++

## Physical servers

@ul
- One OS for each server
  - Some Linux
  - Windows server
@ulend

+++

## Problems

@ul
- Costs
  - Hardware
  - License
  - Light
  - Network
  - Time
- Unused capacity
@ulend

+++

## Solution

@ul
- Virtualization
- Several VM over a hypervisor
@ulend

+++

@ul
- One server, severals virtualized OS
- Less physical servers
- Less cost
  - Hardware
  - Network
  - Light
  - Time
- Optimazed capacity
@ulend

+++

## Problems

@ul
- Each VM requires a minimum of RAM, Disk, CPU
  - Each OS on VM requires a full installation
- Costs of configuration
  - Open/Close ports
  - Install specific libraries
  - All necessary OS configuration
@ulend

+++

## Solution
@ul
- Containers
  - One container for each application
  - All container over one OS
  - The container share the OS resources
- Advantages
  - No OS
  - Light weight
  - Fast start up
@ulend

+++

## Why not?

@ul
- Just install all the application on OS
  - Same port
  - Same application use all RAM (JAVA?)
  - Distinct version for each application
    - Java7, Java8
    - Python 2.7, Python 3.5
  - High CPU
@ulend

+++

## Containers

@ul
- Isolation
- CPU limited
- Network limited
- Each container with its own Python
@ulend

---

## From dotCloud to Docker

+++

@ul
- PaaS
  - Heroku
  - MS Azure
  - GCP
- AWS
- Container
- Docker
@ulend

+++

## Docker
@ul
Docker is nothing more than a collection of technologies to facilitate the deploy and execution of our applications
@ulend

+++

## Technologies
@ul
- Docker Engine
  - Control the containers
  - OS communication
- Docker Compose
  - Manage several containers
- Docker Swarm
  - Manage several Docker Engines (Cluster)
- Docker Hub/Store
- Docker Machine
- Docker Tool Box
@ulend

+++

Open Source

+++

Hello World!!!

---

## Images

+++

@ul
- Read only
- Layers
  - Shared layers
@ulend

+++

## Some commands

+++

@ul
- docker run image
- docker run -it image
- docker run -it --name image
- docker ps
- docker ps -a
- docker start container
- docker start -i container
- docker stop container
- docker rm container
- docker rmi image
- docker image prune
- docker container prune
@ulend

---

## Volumes

+++

Data persistence

+++

## Some commands

+++

@ul
- docker inspect container
- docker run -v "docker-path" image command
- docker run -v "local-path:docker-path" image command
- docker run -p local-port:docker-port -v "local-path:docker-path" image command
- docker run -p local-port:docker-port -v "local-path:docker-path" -w "working-dir" image command
@ulend

---

## My precious

+++

## My image

+++

## Dockerfile

+++

## Main commands
@ul
- FROM
- MAINTAINER
- COPY
- WORKDIR
- RUN
- EXPOSE
- ENTRYPOINT
@ulend

+++

## Some commands

+++

@ul
- docker build path-to-dockerfile 
- docker build -f Dockerfile path-to-dockerfile 
- docker build -f Dockerfile -t username/image-name path-to-dockerfile
- docker login
- docker push username/image-name
- docker pull username/iamge-name
@ulend

+++

## Sample
```
FROM python
MAINTAINER Denis Germano
COPY . /code/grupy
WORKDIR /code/grupy/project
RUN pip install django
RUN django-admin startproject project .
RUN ./manage.py migrate
ENTRYPOINT ./manage.py runserver 0:8000
EXPOSE 8000
```
---

## Network

+++

@ul
- Default: bridge
  - Access only through IP
- Create a new network to access through the name
@ulend

+++

## Some commands

+++

@ul
- docker network create name
@ulend

---


## What's next
@ul
- Docker Compose
- Docker Swarm
- Kubernetes
@ulend
---

### Thank you


