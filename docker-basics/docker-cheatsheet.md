
##Images
docker images
docker build -t myapp:1.0


##Containers
docker ps -a
docker run -it ubuntu bash
docker stop <id> && docker rm <id>

##Debugging
docker logs <id>
docker exec -it <id> sh
docker inspect <id>

