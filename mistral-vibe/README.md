# Building the Docker image

```bash
docker build -t vibe:2.25.0 .
```

# Running the Docker container

Run the Docker container with your workspace mounted into the container's home directory.

```bash
docker run -it --rm -v ~/workspace:/home/vibe/workspace vibe:2.25.0
```
