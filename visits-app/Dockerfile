# Base image
FROM node:alpine

# run commands on the image container

WORKDIR '/usr/app'

COPY package.json .

RUN npm install

COPY . .

CMD [ "npm", "start" ]
