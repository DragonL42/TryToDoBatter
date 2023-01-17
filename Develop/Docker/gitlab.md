# GitLab

### compose-file
```yml
services:
  gitlab:
    image: gitlab/gitlab-ce
    container_name: gitlab
    restart: always
    ports:
      - 114:80
    volumes:
      - /root/docker-data/gitlab/config:/etc/gitlab
      - /root/docker-data/gitlab/logs:/var/log/gitlab
      - /root/docker-data/gitlab/data:/var/opt/gitlab
```

### 首次登录
- 用户名: root
- 密码: gitlab/config/initial_root_apssword中
