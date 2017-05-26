# Memcached Alpine

A minimal Supervisor managed Memcached deamon for docker using the latest Alpine Linux.


## Usage
Pull and run

```bash
docker pull theodesp/memcached-alpine
docker run -i --name memcached -p 10022:22 -p 11211:11211 `docker images -q theodesp/memcached-alpine`
```

## Netcat Examples
Connect to the container and use netcat to check the server

```bash
docker run -it `docker ps -aqf "name=memcached"` /bin/sh
  
# Stats
echo -e "stats" | nc localhost 11300

```

## Licence
MIT
