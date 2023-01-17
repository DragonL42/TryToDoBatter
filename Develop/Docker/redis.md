# Redis

### compose-file
```yml
version: '3.6'
services:
  redis:
    image: redis
    container_name: redis
    environment:
      - TZ=Asia/Shanghai
    volumes:
      - /root/docker-data/redis/conf/redis.conf:/etc/redis.conf
      - /root/docker-data/redis/data:/data
    command:
      redis-server /etc/redis.conf
    deploy:
      replicas: 1
      restart_policy:
        condition: any # on-failure
      resources:
        limits:
          cpus: "1"
          memory: 512M
      update_config:
        parallelism: 1
        delay: 5s
        monitor: 10s
        max_failure_ratio: 0.1
        order: start-first
    ports:
      - 6379:6379
    networks:
      - devenet
    restart: always
networks:
  devenet:
    external:
      name: devenet
```


