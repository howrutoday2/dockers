# dockerfiles-ubuntu-user-adderable
Ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t howrutoday2/ubuntu .
	docker run -it --name u1 -e USER=howrutoday2 -e PASSWD=howrutoday2 howrutoday2/ubuntu
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        howrutoday2/ubuntu      "/bin/bash"         7 seconds ago       Up 6 seconds                            u1
```

To test, ("nowage" is username. )
```
	su - howrutoday2
```
To Rollback
```
    docker rm u1 -f
    docker rmi howrutoday2/ubuntu
```
