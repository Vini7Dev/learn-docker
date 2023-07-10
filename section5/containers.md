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

# List, Start, Stop and Remove Containers

```shell
  # List containers
  docker ps
  
    # Show hidden containers
    docker ps -a

  # Start container
  docker start {CONTAINER NAME OR ID}
  
  # Stop container
  docker stop {CONTAINER NAME OR ID}

  # Remove container
  docker remove {CONTAINER NAME OR ID}
  
    # Remove container with "force" option
    docker remove -f {CONTAINER NAME OR ID}
```

# Container Logs

```shell
  # View container logs
  docker logs --help

  docker logs {CONTAINER NAME OR ID}

  docker logs {OPTION} {CONTAINER NAME OR ID}
    docker logs -f {CONTAINER NAME OR ID}

    docker logs -n {LINES COUNT} {CONTAINER NAME OR ID}

    docker logs -t {CONTAINER NAME OR ID}
```

# Run Commands on Container

```shell
  # Run command on container
  docker exec {CONTAINER NAME OR ID OR NAME} {COMMAND}

    # Example
    docker exec {CONTAINER NAME OR ID OR NAME} ls
```
