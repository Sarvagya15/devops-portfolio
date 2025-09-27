# Docker Compose Demo

This project demonstrates how to use Docker Compose to run multiple containers (Nginx + Redis) with a single configuration file.

## Steps

### 1. Create docker-compose.yml
```yaml
version: "3"
services:
  web:
    image: nginx
    ports:
      - "8081:80"
  redis:
    image: redis

2. Start containers

docker-compose up -d

3. Verify containers

docker ps

4. Test in browser

Visit: http://localhost:8081
 → Nginx Welcome Page.

5. Stop containers

docker-compose down



