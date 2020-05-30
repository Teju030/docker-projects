Docker file -> docker client -> docker server -> build usable image

While modifying the Dockerfile, add new changes to lower section of the file
This way it takes less time to build an image 

Tagging docker image

> docker build -t tejuthegreat/redis:latest <directory_to_be_build>

tag format :    
<docker_user_name>  /  <project_name>: <version>

# Docker image from container

> docker commit -c 'CMD["redis-server"]' <container_id>

Mapping locahost port to container port 
> docker run -p 8080:8080 tejuthegreat/nodejs-app

