# Base image
FROM node:alpine 

# some additional modules
WORKDIR /usr/myapp
COPY ./package.json ./
RUN npm install
COPY ./ ./

# command once the container is spun up
CMD [ "npm", "start" ]
