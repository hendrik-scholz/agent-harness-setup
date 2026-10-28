# Building the Docker image

```bash
docker build -t claude-code:2.1.312 .
```

# Running the Docker container

Run the Docker container with your workspace mounted into the container's home directory.

```bash
docker run -it --rm -v ~/workspace:/home/claude/workspace claude-code:2.1.312
```

The ```/voice``` command in Claude Code only works if your host sound card is added to the container and the container recognizes the sound card. See https://docs.docker.com/reference/cli/docker/container/run/#device.