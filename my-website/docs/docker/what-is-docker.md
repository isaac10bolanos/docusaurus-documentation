---
sidebar_position: 1
sidebar_label: 'Docker'
---

# Docker

## What is Docker?

Docker is a platform and toolset for developing, shipping, and running applications. It uses containerization technology to package an application and its dependencies into a single, portable unit called a container. These containers can be easily moved between different environments, such as development, testing, and production, without any changes to the underlying infrastructure.

## Container

Containers are lightweight, stand-alone, and executable packages that contain everything needed to run an application, including the code, runtime, system libraries, and settings. Containers are isolated from each other and share the host operating system's kernel, making them efficient and resource-friendly.

## Docker Images

Docker images are read-only templates used to create containers. They contain a snapshot of an application and its dependencies at a specific point in time. Images are typically stored in registries (e.g., Docker Hub) and can be versioned.

## Docker Engine

The Docker Engine is the core component responsible for running containers on a host machine. It includes a server, REST API, and a command-line interface (CLI) for interacting with Docker.

## Dockerfile 

A Dockerfile is a text file that defines the instructions for building a Docker image. It specifies the base image, adds application code, sets environment variables, and configures other settings necessary for the container.

## Docker Compose

Docker Compose is a tool for defining and running multi-container applications. It uses a YAML file to describe the services, networks, and volumes required for an application, allowing you to manage complex setups easily.

## Docker Registry

A Docker registry is a repository for storing and distributing Docker images. Docker Hub is a popular public registry, but organizations can also set up private registries for security and compliance reasons.