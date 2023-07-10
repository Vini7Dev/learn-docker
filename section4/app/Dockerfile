FROM node:12-alpine

WORKDIR /app

# RUN addgroup dev_group && adduser -S -G some_user dev_group

# USER some_user

COPY . .

RUN apk add --no-cache python2 g++ make

RUN yarn install --production

EXPOSE 3000

CMD ["node", "/src/index.js"]
