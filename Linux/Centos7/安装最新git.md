# 安装最新git

### 安装使用yum安装需要用到的依赖包
```shell
yum install -y wget
yum install gcc
yum install gcc-c++
yum install -y zlib-devel
yum install -y perl-ExtUtils-MakeMaker package
yum install curl-devel expat-devel gettext-devel
```

### 去官网仓库下载最新的Git版本
[各版本列表](https://mirrors.edge.kernel.org/pub/software/scm/git/)
```shell
wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.18.0.tar.gz
```

### 解压
```sh
tar -zxvf git-2.18.0.tar.gz
cd git-2.18.0
```

### 配置
```sh
./configure --prefix=/usr/local/git
```

### 编译
```sh
make
```

### 安装
```sh
make install
```

### 配置全局环境变量PATH
```sh
echo "export PATH=$PATH:/usr/local/git/bin">>/etc/bashrc
source /etc/bashrc
```

### 验证
```sh
git --version
```

> 如果使用 git --version命令查看的git版本不是自己安装的版本的话，卸载不是自己安装的Git。然后重新生效下环境变量就可以了。

```sh
sudo yum remove git
source /etc/bashrc
git --version
```