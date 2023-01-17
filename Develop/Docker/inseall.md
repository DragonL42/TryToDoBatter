# 安装docker
[官网](https://docs.docker.com/engine/install/)

### Centos8安装Docker

#### 设置存储库
```
yum install -y yum-utils

yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
#### 安装 Docker 引擎
```
sudo yum install docker-ce docker-ce-cli containerd.io
```

#### 启动
```
systemctl start docker
```

#### 设置自启动
```
systemctl enable docker
```
