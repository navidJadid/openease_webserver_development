### Delete all containers
docker rm $(docker ps -a -q)

### Delete all images
docker rmi $(docker images -q)

### Delete all volumes
docker volume rm $(docker volume ls -q --filter dangling=true)
