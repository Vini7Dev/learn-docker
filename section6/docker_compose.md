# Running and Stoping Docker Compose

```shell
  # [WITH BUILD] Create images and containers in background and start
  docker-compose up -d --build

  # [BEFORE BUILD] Create images and containers in background
  docker-compose up -d

  # Stopping docker compose
  docker-compose down
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
