# Docker Volume Demo

This project demonstrates how Docker volumes can be used to persist data even when containers are removed and recreated.

## Steps

### 1. Create a named volume
```bash
docker volume create mydata

2. Run an Nginx container with the volume attached

docker run -d --name vol-nginx -p 8080:80 -v mydata:/usr/share/nginx/html nginx

3. Write a custom index.html inside the container

docker exec -it vol-nginx bash
echo "<h1>Hello from Docker Volume</h1>" > /usr/share/nginx/html/index.html
exit

4. Test in browser

Visit: http://localhost:8080

👉 It's seen as : Hello from Docker Volume

5. Remove and recreate container (data should persist)

docker rm -f vol-nginx
docker run -d --name vol-nginx -p 8080:80 -v mydata:/usr/share/nginx/html nginx

On refresh of browser → custom page is still there 

