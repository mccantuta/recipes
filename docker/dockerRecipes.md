# Docker recipes

## Images
List all images
```
docker images -a
```
Delete image
```
docker rmi <imageId>
```
Delete all images
```
docker rmi $(docker images -a -q)
```
## Containers
List all containers
```
docker ps -a
```
Delete container
```
docker rm <containerId>
```
Delete all containers
```
docker rm $(docker ps -a -q)
```
Build a container
```
docker build -t myorg/myapp .
```
Stop a container
```
docker stop <containerName>
```

## Volumes
List all volumes
```
docker volume ls
```
Delete volumen
```
docker volume rm <volumeId>
```
Find volumes not associated to any container
```
docker volume ls -f dangling=true
```
## Execute commands
Execute bash on docker container
```
docker exec -it <containerName> bash -l
docker exec -it <containerName> /bin/bash
```
## Copy a file to container
Copy a file from local to container
```
docker cp </path/filename> <containerName>:</toPath/toFilename>
```
## Execute PostgresSQL database
Execute PostgreSql database as docker container
```
docker run --rm --name pg-docker -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=password -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data postgres
```
