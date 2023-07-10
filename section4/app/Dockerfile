FROM node:12-alpine

WORKDIR /app

COPY . .

RUN apk add --no-cache python2 g++ make

RUN yarn install --production

EXPOSE 3000

CMD ["node", "/src/index.js"]
