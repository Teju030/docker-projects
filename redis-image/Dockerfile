# Use existing docker image as a base image
FROM alpine 

# Download and install a dependency 
RUN apk add --update redis

# Specify a command for a docker after it starts
CMD ["redis-server"]