#Docker road map

##Table of contents

###Installation
- Docker Install
- Terminal/CLI Tools
- Download the repo


- CRUD of containers
- Process
- Shell containers
- Docker Networking

- Images
- Make Docker files
- Push Custom Images
- Build Images

- Persistent data
- Container Lifetime
- Docker Volumes
- Bind Mounts


- Docker Compose
- Do's and Dont's
- docker-compose.yml
- docker-compose up

- Docker swarm
- Build a cluster
- overlay Networks
- Routing Mesh
- Swarm services
- Stacks
- secrets
- App Deploy lifecycle


##Topic 1
##Docker Editions
Docker community Edition vs Docker Enterprise Editions
three major types of installs: Mac/win, Cloud(AWS, google, Azure)
Linux
windows

###CE vs EE, Stable vs. Edge
CE - Free
EE - Paid
EE has extra features
Edge - Beta, released monthly
Stable - released quarterly

###Using the first container

###docker command
docker [command] [subcommand] [options]

shortcut extension has been added

###Using the first container
docker command
docker command subcommand options

####Image vs Container
Image is the application we want to Routing
Container is an instance of that image running as a Process
you can have many containers running off the same image
Docker default image is registry is called the Docker Hub

###First Container example commands
docker container run --publish 80:80 --detach nginx
docker container ls -a
docker container stop [container unique ID]
docker container run --publish 80:80 --detach --name [container name] nginx
docker container logs [container name]
docker container rm [container]
docker container rm -f [container number]

#Assignment : Run Multiple dockers:
docker container run -d -p 3306:3306 --name db -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql #mysql image
docker container run -d -p 8080:80 httpd #apache server
docker container run -d --name proxy -p 80:80 nginx #nginx server
##remove images
docker container rm -f db proxy ddd #remove all the containers

###what happening inside the container
docker container top mysql
docker container inspect mysql

###Getting the shell inside the container
docker container run -it -> start new container interactively
docker container exec -it -> run additional command in existing container

docker container run -it --name proxy nginx bash
ls -al
exit

docker container start -ai ubuntu - start the container again in the interactive mode

docker container exec -it mysql bash - enter into the already running container with the interactive mode

docker pull alphine
docker container run -it alphine sh

###Docker Networking
