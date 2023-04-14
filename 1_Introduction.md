# Introduction

![Minecraft docker-compose](./images/minecraft_docker-compose.png)

Minecraft is an extremely popular game centered around crafting and survival. It is possible to run your own, or lease a server from a vendor for a monthly fee. There are also options that would allow you to create your server on your local workstation using a containerized version of the server software.

In this lesson you will learn how to deploy a local version of Minecraft using the Docker Desktop software for Mac or Windows. If you are running a Linux based Operating system the docker and docker-compose packages would need to be installed.

The `docker-compose.yaml` manifest file provided for this exercise has all the information needed to build the following:
- The Minecraft server container which includes:
  - Persistent storage
  - Network port mapping
  - Environment variables to declare configuration parameters
  - Automatic restart of unhealthy container
- Minecraft backup agent container which includes:
  - Persistent storage
  - Backup scheduling
  - Old backup pruning to prevent storage issues
  - Automatic restart of unhealthy container

Once the docker-compose file has been instantiated, the containers will be pulled and started up. The first time this process runs it takes a little longer since it needs to download the containers and cache them. Additionally, the first time the container is run it installs the Minecraft service and downloads the plugins selected in the manifest.

[![continue](./images/continue.png)](./2_How_It_Works.md)