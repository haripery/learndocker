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
docker container stop 630
docker container run --publish 80:80 --detach --name webhost nginx
