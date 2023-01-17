
### 安装zsh并切换

#### linux-centos7
```shell
# 安装基础库
yum install git
yum install vim
yum install zsh

# 安装oh-my-zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 切换默认zsh
chsh -s /bin/zsh
```

### oh-my-zsh插件
#### 自动补全zsh-autosuggestions
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
### 命令高亮zsh-syntax-highlighting
```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
