# Portainer管理界面

#### 安装Portainer管理界面
```sh
docker pull portainer/portainer-ce
```

#### 启动Portainer容器
```sh
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock --restart=always --name portainer portainer/portainer-ce
```