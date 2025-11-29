---
title: Docker Containers Overview
linkTitle: Docker Container
date: 2025-11-29
weight: 30
---

## Docker Containers
A Docker container is a lightweight, standalone, and executable package that includes everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings. Containers are created from Docker images and provide an isolated environment for applications to run consistently across different computing environments.

### Key Concepts of Docker Containers
- **Isolation**: Each Docker container runs in its own isolated environment, ensuring that applications do not interfere with each other. This isolation is achieved through containerization technology, which uses features of the host operating system.
- **Portability**: Docker containers can run on any system that has Docker installed, making it easy to move applications between different environments, such as development, testing, and production  
- **Lightweight**: Containers share the host operating system's kernel, making them more lightweight than traditional virtual machines. This allows for faster startup times and lower resource consumption.
- **Ephemeral**: Docker containers are designed to be temporary and can be easily created,
  stopped, and deleted. However, data can be persisted using Docker volumes.

---

### Commands to Work with Docker Containers
Here are some common Docker commands related to containers:

### Run a Container (`run`)
To create and start a new Docker container from an image, use the `docker run` command:

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

Example:

```bash
docker run -d -p 80:80 nginx
```

This command runs an Nginx container in detached mode (`-d`) and maps port 80 of the host to port 80 of the container.

### List Running Containers (`ps`)
To list all currently running Docker containers, use the following command:

```bash
docker ps
```

or

```bash
docker container ls
```

Note:
`ps` stands for `process status`

### Create a Container (`create`)
To create a new Docker container without starting it, use the `docker create` command:

```bash
docker create [OPTIONS] IMAGE [COMMAND] [ARG...] [CONTAINER NAME]
```

Example:

```bash
docker create --name my_nginx -p 80:80 nginx
```
This command creates a new Nginx container named `my_nginx` without starting it.

### Stop a Container (`stop`)
To stop a running Docker container, use the `docker stop` command followed by the container ID or name:

```bash
docker stop <container_id_or_name>
```

Example:

```bash
docker stop my_nginx
```

Example using container ID:

```bash
docker stop 1a2b3c4d5e6f
```

### Remove a Container (`rm`)
To delete a Docker container, use the `docker rm` command followed by the container ID or name:

```bash
docker rm <container_id_or_name>
```

Example:

```bash
docker rm my_nginx
```

Example using container ID:

```bash
docker rm 1a2b3c4d5e6f
```

### List All Containers (`ps -a`)
To list all Docker containers, including those that are stopped, use the following command:
```bash
docker ps -a
```

or

```bash
docker container ls -a
```
Note:
`-a` stands for `all`

### Start a Container (`start`)
To start a stopped Docker container, use the `docker start` command followed by the container ID or name:

```bash
docker start <container_id_or_name>
```

Example:

```bash
docker start my_nginx
```

Example using container ID:

```bash
docker start 1a2b3c4d5e6f
```

### Restart a Container (`restart`)
To restart a running or stopped Docker container, use the `docker restart` command followed by the
container ID or name:

```bash
docker restart <container_id_or_name>
```

Example:

```bash
docker restart my_nginx
```

Example using container ID:

```bash
docker restart 1a2b3c4d5e6f
```

## Summary of Commands
| Command                     | Description                                      | Example                                 |
|-----------------------------|--------------------------------------------------|-----------------------------------------|
| `docker run`                | Create and start a new Docker container          | `docker run -d -p 80:80 nginx`            |
| `docker ps`                 | List
  all running Docker containers                  | `docker ps`                             |
| `docker create`             | Create a new Docker container without starting it | `docker create --name my_nginx -p 80:80 nginx` |
| `docker stop <container>`   | Stop a running Docker container                  | `docker stop
  my_nginx`                          |
| `docker rm <container>`     | Remove a Docker container                        | `docker rm my_nginx`                    |
| `docker ps -a`              | List all Docker containers (running and stopped) | | `docker ps -a`                          |
| `docker start <container>`  | Start a stopped Docker container                  | `docker start my_nginx`                 |
| `docker restart <container>` | Restart a running or stopped Docker container | `docker restart my_nginx`                |

### Additional Information
For more detailed information on Docker containers and additional commands, refer to the official Docker documentation: [https://docs.docker.com/engine/reference/commandline/container/](https://docs.docker.com/engine/reference/commandline/container/)
