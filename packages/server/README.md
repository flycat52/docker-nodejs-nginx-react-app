# docker-nodejs-nginx-react-app/server

Server app component of docker-nodejs-nginx-react-app

Cloned from [docker-nodejs-nginx-app](https://github.com/EdgeJay/docker-nodejs-nginx-app)

## Getting Started

### Install dependencies

1. `touch .env && echo "NODE_PORT=4000" > ./.env`
2. `yarn install`

### Start server in development mode

`yarn run dev`

Open http://localhost:4000/api/hello

### Deploy server as via Docker compose

In this setup, all requests to server app are passed through nginx container "app_nginx" first. Nginx container is listening at port 8080.

`yarn run docker:deploy`

Open http://localhost:8080/api/hello

### Deploy server as standalone Docker container

In this setup, server app is running as a standalone Docker container and exposes port 4000 to Docker host.

`yarn run docker:build`
`yarn run docker:run`

### Other scripts

### yarn run docker:build

Re-build server app Docker image

### yarn run docker:run

Deploy and run container from server app Docker image