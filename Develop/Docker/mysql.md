# mysql


### compose-file
```yml
version: "3"
services:
  mysql:
    image: mysql:5.7
    container_name: mysql
    environment:
      - MYSQL_ROOT_PASSWORD=root
    volumes:
      - /data/docker/mysql/conf/mysql.cnf:/etc/mysql/my.cnf
      - /data/docker/mysql/logs:/var/log
      - /data/docker/mysql/data:/var/lib/mysql
    ports:
      - 3306:3306
    restart: always
    networks:
      - basenet
networks:
  basenet:
    external:
      name: basenet
```
