
## 安装jupyter notebook

```shell
conda install jupyter notebook
```

## 运行
```shell
jupyter notebook -h

jupyter notebook
```

## 配置
```shell
# 这条命令虽然可以用于查看配置文件所在的路径
# 但主要用途是是否将这个路径下的配置文件替换为默认配置文件
# 第一次没有配置文件时可以使用此命令生成
jupyter notebook --generate-config

# 默认保存位置
vim ~/.jupyter/jupyter_notebook_config.py
```

## 关联conda
```shell
# 安装插件
conda install nb_conda
```

## 安装插件nbextensions
```shell

pip install jupyter_contrib_nbextensions

jupyter contrib nbextension install --user

# 激活代码提示插件
# hinterland
```
