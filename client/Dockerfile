# syntax=docker/dockerfile:1
FROM node:14-alpine

LABEL Maintainer Becky

WORKDIR /usr/src/client

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

RUN npm install -g serve

EXPOSE 3000

CMD [ "serve", "-s", "build", "-l", "3000" ]