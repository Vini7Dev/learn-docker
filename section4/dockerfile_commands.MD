# Dockerfile

> FROM: Image name (ubunto, alpine, ...) and platform (nodejs, python, ...)
> WORKDIR: Set a default directory of image for the next commands (/app, ...)
> COPY: Copy all files from application to Docker Image
> ADD: Copy files from internet or zip folders to Docker Image
> ENV: Set environment settings
> EXPOSE: Expose an container port for access
> USER: Who is the user who will run the application
> RUN: To start the application (During image construction)
> CMD / ENTRYPOINT: Run commands (During image initialization)

## Examples

```Dockerfile
  # FROM
  FROM node:12-alpine

  # WORKDIR
  WORKDIR /directory

  # COPY
  COPY file1.json file2.json .

  COPY file1.json .

  COPY *.json .

  COPY . .

  # ADD
  ADD https://example.com/file1.json .

  ADD file.zip .

  # RUN
  RUN apk add --no-cache python2 g++ make

  RUN yarn install --production

  # USER
  RUN addgroup dev_group && adduser -S -G some_user dev_group
  USER some_user

  # ENV
  ENV API_URL=https://example.com

  # EXPOSE
  EXPOSE 3000

  # CMD
  CMD ["node", "src/index.js"]
```

# Create Image with Tags (Version Control)

```shell
  # Create Image
  docker build -t {IMAGE NAME}:{VERSION TEXT} . # . = Current directory
    # docker build -t app:v1.0.0 .

  # Rename Image Tag
  docker image tag {IMAGE NAME}:{IMAGE TAG} {IMAGE NAME}:{NEW IMAGE TAG}
    # docker image tag app:latest app:v1.0.0

  # Create Container from Image
  docker run {IMAGE NAME} -p {CONTAINER PORT}:{PC PORT}

  # Or, on interactive mode
  docker run -it {IMAGE NAME} -p {CONTAINER PORT}:{PC PORT}
```

# Upload Image to Docker Hub

> ATT: The image tag must be the same as the repository name

```shell
  # Make login on docker hub
  docker login

  # First version upload
  docker push {REPOSITORY NAME}:{VERSION}

  # Uploading other versions
  docker push {REPOSITORY NAME}:{OTHER VERSION}
```
