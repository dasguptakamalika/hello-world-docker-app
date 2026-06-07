# Dockerized Hello World Spring Boot Application

## Overview

This project demonstrates how to containerize a simple Spring Boot web application using Docker.

The application exposes a single REST endpoint and returns a greeting message. Docker is used to package the application and its dependencies into a portable container, ensuring consistent behavior across different environments.

---

## Prerequisites

Before running the application, make sure the following are installed:

* Docker Desktop
* Git (optional, for cloning the repository)

---

## Build the Docker Image

From the project root directory, run:

```bash
docker build -t simpleapp .
```

This command builds a Docker image named `simpleapp`.

---

## Verify the Image

To confirm the image was created successfully:

```bash
docker images
```

You should see an image named `simpleapp`.

---

## Run the Docker Container

Start the application inside a Docker container:

```bash
docker run -p 8081:8080 simpleapp
```

Port mapping:

* Container port: `8080`
* Host port: `8081`

---

## Test the Application

Open a new terminal and run:

```bash
curl http://localhost:8081
```

Expected output:

```text
Hello World <3
```

---

## Verify the Running Container

To view running containers:

```bash
docker ps
```

You should see the container running with a port mapping similar to:

```text
0.0.0.0:8081->8080/tcp
```

---

## Project Structure

* `src/` - Spring Boot application source code
* `Dockerfile` - Docker image definition
* `README.md` - Project documentation
* `screenshots/` - Screenshots showing image build, container execution, and verification steps

---

## Why Docker?

Docker packages the application together with its runtime environment and dependencies, 
allowing it to run consistently across development, testing, and production environments without requiring additional setup.
Pretty cool !
