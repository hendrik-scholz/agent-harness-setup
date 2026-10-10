# Agent Harness Setup

## Building the Docker image

Build the Docker image from the Dockerfile in the alpine or ubuntu directory.

```bash
docker build -t pi-dev:1.1.0 .
```

## Running the Docker container

Run the Docker container with your workspace mounted into the container's home directory.

```bash
docker run -it --rm -v ~/workspace/project:/home/pi/workspace/project pi-dev:1.1.0
```

