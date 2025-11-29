---
title: Docker Images Overview
linkTitle: Docker Image
date: 2025-11-27
weight: 20
---

## Docker Images
A Docker image is a lightweight, standalone, and executable software package that includes everything needed to run a piece of software, including the code, runtime, libraries, environment variables, and configuration files. Docker images are used to create Docker containers, which are instances of the images that can be run on any system with Docker installed.

### Key Concepts of Docker Images
- **Layered Architecture**: Docker images are built in layers, where each layer represents a set of file changes or additions. This layered approach allows for efficient storage and sharing of images, as common layers can be reused across different images.
- **Immutability**: Once a Docker image is created, it is immutable, meaning it cannot be changed. Any modifications to the image require creating a new image based on the original.
- **Versioning**: Docker images can be versioned using tags, allowing users to specify and manage different versions of an image easily.
- **Registries**: Docker images are stored in registries, which are repositories for sharing and distributing images. The most common public registry is Docker Hub, but private registries can also be set up for internal use.

---

## Commands to Work with Docker Images
Here are some common Docker commands related to images:

### See Available Images (`images`)
To list all Docker images available on your local system, use the following command:
```bash
docker images
```
or

```bash
docker image ls
```

### Pull an Image (`pull`)
To download a Docker image from a registry, use the `docker pull` command followed by the image name:
```bash
docker pull <image_name>

docker pull <image_name>:<tag>
```
Example without tag (defaults to "latest"):
```bash
docker pull nginx
```
Example with tag and specific version:
```bash
docker pull nginx:latest

docker pull nginx:1.21.6
```

### Pull an Image from a Specific Registry (`pull` with registry)
To pull an image from a specific registry, include the registry URL in the image name:
```bash
docker pull <registry_url>/<image_name>:<tag>
```
Example:
```bash
docker pull myregistrydomain.com/myimage:mytag
```

### Remove an Image (`rmi` or `image rm`)
To delete a Docker image from your local system, use the `docker rmi` command followed by the image name or ID:
```bash
docker rmi <image_name_or_id>
```
or
```bash
docker image rm <image_name_or_id>
```
Example:
```bash
docker rmi nginx:latest

docker image rm nginx:latest
```

## Summary of Commands
| Command                     | Description                                      | Example                                 |
|-----------------------------|--------------------------------------------------|-----------------------------------------|
| `docker images`             | List all Docker images on the local system       | `docker images`                         |
| `docker pull <image_name>`  | Download a Docker image from a registry            | `docker pull nginx`                     |
| `docker pull <image_name>:<tag>` | Download a specific version of a Docker image | `docker pull nginx:1.21.6`            |
| `docker pull <registry_url>/<image_name>:<tag>` | Pull an image from a specific registry | `docker pull myregistrydomain.com/myimage:mytag` |
| `docker rmi <image_name_or_id>` | Remove a Docker image from the local system | `docker rmi nginx:latest`               |
| `docker image rm <image_name_or_id>` | Remove a Docker image from the local system | `docker image rm nginx:latest`           |

### Additional Resources
- [Docker Official Documentation on Images](https://docs.docker.com/engine/reference/commandline/image/)
- [Docker Hub](https://hub.docker.com/) - A public registry for Docker images
- [Creating Docker Images](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
