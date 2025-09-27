# Docker Volume Cheatsheet

## Create a volume
docker volume create mydata

## List volumes
docker volume ls 

## Inspect volume
docker volume inspect mydata

## Run container with volume 
docker run -d --name test -v mydata:/data alpine

## Remove container (data persists in volume)
docker rm -f test

## Start new container with same volume
docker run -it --rm -v mydata:/data alpine sh

# Inside container data is still there
