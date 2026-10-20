# Agent Harness Setup

The pi folder contains a configuration for setting up a lightweight development environment, including a Dockerfile and MCP server configuration (mcp.json). These files are used to create and configure a containerized environment for AI-assisted coding tasks.

## Building the Docker image

Build the Docker image from the Dockerfile in the pi directory.

```bash
docker build -t pi:1.3.0 .
```

## Running the Docker container

Run the Docker container with the time zone set and your workspace mounted into the container's home directory.

```bash
docker run -it --rm -e TZ=America/Toronto -v ~/workspace:/home/pi/workspace pi:1.3.0
```
