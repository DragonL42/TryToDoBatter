# ip设置

### 进入目录
```sh
cd /etc/sysconfig/network-scripts/
```

### 编辑文件
> 根据自身情况修改文件，每个系统的文件名不一致
> 可通过ip addr进行查询
```sh
vi ifcfg-en33
```

### 配置文件详情
- BOOTPROTO: 开机协议，有dhcp及static
- ONBOOT: 设置为开机启动
- DNS1: DNS地址,国内可选择114.114.114.114
- IPADDR: IP地址，192.168.x.0-255之间都可以
- NETMASK: 子网掩码255.255.255.0
- GATEWAY: 网关

### 重启网络
```sh
service network restart
```

### 测试网络
```sh
ping www.baidu.com
```