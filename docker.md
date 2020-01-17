# Docker Commands

>### List all local docker images

    docker images

>### List running docker containers

    docker ps

>### List all docker containers

    docker ps -a

>### Run docker image with port forwarding

    docker run -itd -P tomcat

## Docker Machine

>### Docker Machine will create a virtual machine where docker engine is running and ready to run docker images as required.

Install on Linux (centOS)
---

>### Start Docker Service, make sure its running
    
    systemctl start docker

> download docker machine binary and follow instructions as here: https://github.com/docker/machine/releases

>### Use following commands

    sudo su -

    curl -L https://github.com/docker/machine/releases/download/v0.16.2/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine

    chmod +x /tmp/docker-machine

    cp /tmp/docker-machine /usr/local/bin/docker-machine


>### Check docker machine version
    
    docker-machine -version

>### List created docker hosts
    
    docker-machine ls

>### Create New Docker Host
    
    docker-machine create --driver google --google-project project-name-id hostname1

> More details on docker machine driver (cloud provider specific) are available here:
https://docs.docker.com/v17.12/machine/drivers/

>### Check environment variables of created docker host machines

    docker-machine env hostname1

>### Point current shell to the docker daemon of the host

    eval $(docker-machine env hostname1)

>### Confirm which host is currently active

    docker-machine active

>### Unset pointed docker host

    eval $(docker-machine env -u)

## Running docker image as container

>### List Docker Machine, set it active using eval command.

    docker images

    docker run -itd -P nginx

>### Get the IP addres of the docker machine host

    docker-machine ip hostname1

>### See if nginx is runnig

    curl <ip-addr:port>




