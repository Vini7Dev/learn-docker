# Dockerfile

> FROM: Image name (ubunto, alpine, ...) and platform (nodejs, python, ...)
> WORKDIR: Set a default directory of image for the next commands (/app, ...)
> COPY: Copy all files from application to Docker Image
> ADD: Copy files from internet or zip folders to Docker Image
> RUN: To start the application
> ENV: Set environment settings
> EXPOSE: Expose an application port for access
> USER: Who is the user who will run the application
> CMD / ENTRYPOINT: Run commands

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

# ENV
ENV API_URL=https://example.com
```

# Create Image

```shell
  # Create Image
  docker build -t {IMAGE NAME} . # . = Current directory

  # Create Container from Image
  docker run {IMAGE NAME} 

  # Or, on interactive mode
  docker run -it {IMAGE NAME}
```
