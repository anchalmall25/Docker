# *Docker*

![c0fe1677feaff0803fe6f66563a8aef0](https://user-images.githubusercontent.com/62477381/151655716-4a4ef09f-81ba-4498-be1d-c9fac6579bb2.gif)


*Docker container technology was launched in 2013 as an open source Docker Engine.*

Docker containers that run on Docker Engine:

1. Standard: Docker created the industry standard for containers, so they could be portable anywhere
2. Lightweight: Containers share the machine’s OS system kernel and therefore do not require an OS per application, driving higher server efficiencies and reducing server and      licensing costs
3. Secure: Applications are safer in containers and Docker provides the strongest default isolation capabilities in the industry

Lets see some commands of docker:-

## Run A NEW CONTAINER

*To start  Docker Daemon in Linux:-
<br/>`systemctl start docker`*

* Start a new container from an image:-
```
docker run <image-name>
ex-docker run nginx
```

* ..and assign it a name:-
```
docker run --name CONTAINER IMAGE
ex-docker run web nginx
```

* ..and map a port:-
```
docker run -p HOSTPORT:CONTAINERPORT IMAGE
ex-docker run -p 8080:80 nginx
```

* ..and assign it a hostname:-
```
docker run --hostname HOSTNAME IMAGE
ex-docker run --hostname svc nginx
```

## MANAGE CONTAINERS

* Show list of running conatiner:-
<br/>`docker ps`

* Show a list of all conatiner:-
<br/>`docker ps -a`

* Delete a container:-
<br/>`docker rm CONTAINER`

* Delete a running conatiner:-
<br/>`docker rm -f CONTAINER `    

* Delete stopped conatiners:-
<br/>`docker container prune`

* Stop a running conatiner:-
<br/>`docker stop container`

* Start a stopped conatiner:- 
<br/>`docker start cotainer`

* Copy a file from conatiner to the host:-
<br/>`docker cp conatiner:source target`

* Copy a file from host to container:-
<br/>`docker cp target container:source`

* Commit an image out of conatainer:-
<br/>`docker commit container`

## Manage Images

* Download an image:-
<br/>`docker pull image`

* Upload an image to repository:-
<br/>`docker push image`

* Delete an image:-
<br/>`docker rmi image`

* Show list of all images
<br/>`docker images`

* Delete dangling images:-
<br/>`docker image prune`

* Delete all unused images:-
<br/>`docker images prune -a`

* Build a image from a Dockerfile
```
docker build Directory
docker build .
```
## Info and Stats

* Show logs of conatiners:-
<br/>`docker logs container`

* Show stats of running conatiner:-
<br/>`docker stats`

* Get detailed info of conatiner:-
<br/>`docket inspect imagename`

* Show installed version of Docker:-
<br/>`docker version`











