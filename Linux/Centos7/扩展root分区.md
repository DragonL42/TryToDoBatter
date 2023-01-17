# 扩展root分区

> 将`centos-home`的空间拓展到`centos-root`中

### 卸载/home
```sh
umount /home
```

### 移除centos-home分区
```sh
lvremove /dev/mapper/centos-home
```

### 拓展root
> 拓展后确保home还有至少1G空间，最好能多点，防止创建/home时无法创建
```sh
lvextend -L 需要增加的容量 /dev/mapper/centos-root
```
- 事例
    - +132G 增加132G
    - +100%FREE 增加全部可用空间


### 拓展文件系统
```sh
xfs_growfs /dev/mapper/centos-root
```

### 重新创建/home
```sh
lvcreate -L 10G -n /dev/mapper/centos-home
```

### 创建时显示一下内容为失败，建议0.5G适当调整
```sh
Volume group "centos" has insufficient free space (2335 extents): 2560 required.
```
### 显示一下为成功
```sh
Logical volume "home" created.
```

### 重建文件系统
```sh
mkfs.xfs /dev/mapper/centos-home
```

### 挂载
```sh
mount /dev/mapper/centos-home
```


