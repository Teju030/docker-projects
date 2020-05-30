To pull the image from Docker HUb and store it image cache


> docker run <image_name>

e.g.  docker run hello-world  

To override the default command afte docker container  
> docker run <image_name>  <command>

> docker run busybox echo Hi there
> docker run busybox ls

To list all the running container
> docker ps 

To list all containers ever created
> docker ps --all

> docker create hello-world 
> docker start -a <hash_of_container>
-a => print the output coming from container

To remove all `stopped containers`, all `dangling images`, all `build cache`, all networking that is not used by any container
> docker system prune

> docker logs <container_id>

Forcefully termination
> docker kill <container_id>

Gracefully stop
> docker stop <container_id>

To run mutliple commands in docker container
> docker exec -it <container_id> <command>

it = > type input directly into container

To enable shell inside of docker
> docker exec -it <container_id> sh

> docker run -it <container_id> sh


-----------------------------------------------------------------------------
### Terminologies for Linux only
Namespacing -> isolating the resources per process or group of process
Control group -> limit the resources per process to use


### For windows / MAC 
when we install docker desktop, it actually installs a linux virtual machine.
On top of that different docker images are spun up 

------------------------------------------------------------------------------

docker run = docker create + docker start

purpose of `it` flag in docker command 
docker exec -it <container_id> <command>

i = > attach terminal to STDIN channel
t = > all text shows up in formated manner
