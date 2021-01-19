# Docker

Software platform for building applications based on containers.

**Dockerfile** - build instruction on how to build container image. 

**Image** - templates for runing docker containers

**Container** - running instance of image.

---

## Commands

```bash
#---------------
# SYSTEM
#---------------
docker system prune                               # remove unused data
docker system df                                  # show disk usage

#---------------
# BASE
#---------------
docker ps                                         # list all runing containers
docker exec -it <container> bash                  # run command inside container
docker-compose exec <service> bash                # run command inside docker-compose

#---------------
# CONTAINERS
#---------------

docker container ps                               # show running containers
docker ls -a                                      # show all containers

docker container start <options> <container>      # start container
docker container stop <options> <container>       # stop running container
docker container pause <container>                # pause all processes within container
docker container unpause <container>              # unpause all processes within container
docker container restart <options> <container>    # restart container
docker container kill <continer>                  # kill container

docker container rm <container>                   # remove container
docker container prune <options>                  # remove all stopped containers

docker container exec <options> <container> bash  # run command in a container
docker container inspect <options> <container>    # display detailed information
docker container logs <options> <container>       # fetch the logs of a container



#--------------
# IMAGES
#--------------

docker image ls                                   # list images
docker image prune                                # remove unused images
docker image rm <image> -f                        # remove image

```

