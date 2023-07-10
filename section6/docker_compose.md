# Execute Docker Compose

```shell
  # Create images and containers in background
  docker-compose up -d
```

# Docker Compose YAML (Some keywords)

> **Version:** Version of docker compose yaml
> **Services:** One for each container service
> **Depends On:** Run only after other services complete
> **Image:** Create image by image name (on database, for example)
> **Build:** Create image from a directory's Dockerfile (on backend, for example)
> **Ports:** Expose the container ports in the following format: {PC PORT}:{CONTAINER PORT}
> **Volumes:** Create a volume to store the data in permanent memory
> **Environment:** Set environment variables
