Install node js 

To create initial REACT JS empty project
> npx create-react-app frontend

To start dev server
> npm run start 

TO run test associated with project 
> npm run test

> npm run build

Dockerfile.dev => for dev instance

> docker build -f Dockerfile.dev .

> docker run -it -p 3000:3000 CONTAINER_ID

To reflect the hot changes done in project directly in the docker container
Docker volumes similarly ports mapping 

> docker run -p 3000:3000 -v /usr/app/node_modules -v $(pwd):/usr/app  <image_id>

> docker run -it -p 3000:3000 -v /usr/app/node_modules -v ${pwd}:/usr/app 4b024cc69dc4

docker run -it -p 3000:3000 -v /usr/app/node_modules -v ${PWD}:/usr/app -e CHOKIDAR_USEPOLLING=true ee0d7d337261

For windows add in the docker-compose file
```
services:
    environment:
      - CHOKIDAR_USEPOLLING=true
```

Add following line for windows to server. otherwise react server with exist with 0 error code
```
services:
    web:
        stdin_open: true 
```