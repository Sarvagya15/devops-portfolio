# Docker compose cheatsheet

## Start services 
docker-compose up -d 

## Stop services
docker-compose down

## View running services 
docker-compose ps

## View logs 
docker-compose logs -f

## Run one-off command
docker-compose run <service> <command>

## Rebuild images
docker-compose build 

## Scale services 
docker-compose up -d --scale web=3


