# Agent Harness Setup

The alpine folder contains a configuration for setting up a lightweight development environment, including a Dockerfile and MCP server configuration (mcp.json). These files are used to create and configure containerized environments for AI-assisted coding tasks.

## Building the Docker image

Build the Docker image from the Dockerfile in the alpine directory.

```bash
docker build -t pi:1.3.0 .
```

## Running the Docker container

Run the Docker container with your workspace mounted into the container's home directory.

```bash
docker run -it --rm -v ~/workspace:/home/pi/workspace pi:1.3.0
```
