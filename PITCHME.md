## A simple introduction to docker


Denis Germano

Crave Food Systems - August 2018

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
- Docker Hub
- Docker Machine

@ulend

+++

Open Source

---

## Images

---

## Volumes

---

## My precious

+++

## My image

---

## Network

---

## Docker Compose

---

## What's next

---

### Thank you


