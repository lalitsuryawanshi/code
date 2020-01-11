# Docker

```javascript

function hello(){
    return 'Hello';
}


1. Hello
1. Hello


## Docker Machine

### Install on Linux (centOS)

login as root
> sudo su -

download docker machine binary and follow instructions 

https://github.com/docker/machine/releases

```bash
curl -L https://github.com/docker/machine/releases/download/v0.16.2/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine

chmod +x /tmp/docker-machine

cp /tmp/docker-machine /usr/local/bin/docker-machine
```