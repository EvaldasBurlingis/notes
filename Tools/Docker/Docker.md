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
docker system prune 			    # remove unused data
docker system df			        # show disk usage

#---------------
# BASE
#---------------
docker ps 				            # list all runing containers
docker exec -it <container> bash	# run command inside container
docker-compose exec <service> bash  # run command inside specified service in docker-compose

#---------------
# CONTAINERS
#---------------

docker ls -a				        # show all containers
docker restart <container>		    # restart container
docker container kill <continer>	# kill container

#--------------
# IMAGES
#--------------

docker image ls				        # list images
docker image prune			        # remove unused images
docker image rm <image> -f		    # remove image

```

