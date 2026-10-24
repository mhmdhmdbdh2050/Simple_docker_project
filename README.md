# Simple Docker Website

A small Docker Compose example that serves the local `html/` directory with the official Nginx image. Unlike the Docker Custom Image project, this project bind-mounts website files at runtime instead of copying them into a custom image.

## Run

Requirements: Docker Engine and the Docker Compose plugin.

```bash
docker compose up -d
```

Open <http://localhost:8081>. Compose maps host port `8081` to Nginx port `80` and mounts `./html` as the website document root.

## Verify and clean up

```bash
docker compose ps
curl -I http://localhost:8081
docker compose down
```

This is a learning example, not a production web server configuration.
