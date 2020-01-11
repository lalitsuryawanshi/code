# Docker

## Docker Machine

### Install on Linux (centOS)

> download docker machine binary and follow instructions as here: https://github.com/docker/machine/releases

Use following commands
```bash

sudo su -

curl -L https://github.com/docker/machine/releases/download/v0.16.2/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine

chmod +x /tmp/docker-machine

cp /tmp/docker-machine /usr/local/bin/docker-machine

