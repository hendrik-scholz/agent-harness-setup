# Building the Docker image

```bash
docker build -t pi:1.4.0 .
```

# Running the Docker container

Run the Docker container with the time zone set and your workspace mounted into the container's home directory.

```bash
docker run -it --rm -e TZ=America/Toronto -v ~/workspace:/home/pi/workspace pi:1.4.0
```
