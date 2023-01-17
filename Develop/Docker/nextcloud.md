# nextcloud

### compose-file
```yml
version: "2"
services:
  nextcloud:
    image: nextcloud:latest
    container_name: nextcloud
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Asia/Shanghai
    volumes: 
      - /root/docker-data/nextcloud/html:/var/www/html
      - /root/docker-data/nextcloud/custom_apps:/var/www/html/custom_apps
      - /root/docker-data/nextcloud/config:/var/www/html/config
      - /root/docker-data/nextcloud/data:/var/www/html/data
      - /root/docker-data/nextcloud/themes:/var/www/html/themes
    ports:
      - 80:80
    networks:
      - devenet
    restart: always
networks:
  devenet:
    external:
      name: devenet
```
