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

    # With volume
    docker run -v {VOLUME NAME}:{DIRECTORY TO ADD VOLUME}
    
      # Example
      docker run -v {VOLUME NAME}:/app/data
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
  # Open container with shell
  docker exec -it {CONTAINER NAME OR ID} sh

  # Run command on container
  docker exec {CONTAINER NAME OR ID} {COMMAND}

    # Example
    docker exec {CONTAINER NAME OR ID} ls
```

# Working with volumes

```shell
  # Create volume
  docker volume create {VOLUME NAME}

  # View volume info
  docker volume inspect {VOLUME NAME}

  # Associate volume to container
  docker run {...} -v {VOLUME NAME}:{DIRECTORY TO ADD VOLUME}

    # Example
    docker run {...} -v {VOLUME NAME}:/app/data
```
