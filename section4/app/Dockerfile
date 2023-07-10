FROM node:12-alpine

WORKDIR /app

# RUN addgroup dev_group && adduser -S -G some_user dev_group

# USER some_user

COPY package.json .

RUN apk add --no-cache python2 g++ make

RUN yarn install --production

COPY . .

CMD ["node", "src/index.js"]

EXPOSE 3000
