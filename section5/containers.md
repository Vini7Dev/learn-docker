# Create Container

```shell
  # BASE
  docker run -d -p {PC PORT}:{CONTAINER PORT} --name {CONTAINER NAME} {IMAGE NAME}

  # Start container
  docker run {IMAGE NAME}

    # Run on background
    docker run -d {IMAGE NAME}

    # Rename container
    docker run --name {CONTAINER NAME} {IMAGE NAME}

    # With port redirect
    docker run -p {PC PORT}:{CONTAINER PORT} {IMAGE NAME}
```

# Start and Stop Containers

```shell
  # Start
  
```

# Container Logs

```shell
  # View container logs
  docker logs --help

  docker logs {CONTAINER ID}

  docker logs {OPTION} {CONTAINER ID}
    docker logs -f {CONTAINER ID}

    docker logs -n {LINES COUNT} {CONTAINER ID}

    docker logs -t {CONTAINER ID}
```

# Run Commands on Container

```shell
  # Run command on container
  docker exec {CONTAINER ID OR NAME} {COMMAND}

    # Example
    docker exec {CONTAINER ID OR NAME} ls
```
