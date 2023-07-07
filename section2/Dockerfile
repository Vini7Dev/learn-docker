# Platform : SO
FROM node:alpine

# Copy all files from "./" to "/app" on image
COPY . /app

# Set default working directory for the next commands
WORKDIR /app

# Execute the app on "/app/app.js" with "node"
CMD node app.js

# To build this image, run "docker build -t {IMAGE NAME} ."
