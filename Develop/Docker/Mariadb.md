# Mariadb


### compose-file
```yml
version: "2"
services:
  mariadb:
    image: linuxserver/mariadb
    container_name: mariadb
    environment:
      - MYSQL_ROOT_PASSWORD=mysqladmin
    volumes:
      - /root/data/mariadb:/var/lib/mysql
    ports:
      - 3306:3306
    networks:
      - devenet
    restart: always
networks:
  devenet:
    external:
      name: devenet
```
