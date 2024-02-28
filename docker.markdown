# Docker 概述

## Docker 基础

1. **Linux Container (内核虚拟化技术)** 是Docker的底层实现技术。
2. **Docker** 是PaaS提供商dotCloud开源的一个基于LXC (Linux Containers) 的高级容器引擎，源代码托管在GitHub上，基于Go语言并遵从Apache 2.0协议开源。
3. **Docker 设想** 是将交付运行环境标准化，如同海运，其中OS类似于一个货轮，每个在OS基础上的软件都像是一个集装箱。用户可以通过标准化手段自由组装运行环境，集装箱的内容既可以用户自定义，也可以由专业人员制造。

## 云计算服务的三种主要类型

1. **IaaS (Infrastructure as a Service)**: 基础设施即服务
2. **PaaS (Platform as a Service)**: 平台即服务
3. **SaaS (Software as a Service)**: 软件即服务

## Docker 重要概念

- **仓库（Repository）**
- **镜像（Image）**
- **容器（Container）**

## Docker 命令格式

`docker + 命令关键字(COMMAND) + 一系列参数`

### 示例命令

docker run --name MyWordPress --link db:mysql -p 8080:80 -d wordpress

### Docker 基础命令

- `docker info`: 显示Docker系统信息。
- `docker images`: 列出本地镜像。
- `docker search`: 在Docker Hub搜索镜像。
- `docker pull`: 下载镜像到本地。
- `docker rmi`: 删除本地镜像。

### 容器管理命令

- `docker ps`: 列出运行中的容器。
- `docker ps --no-trunc`: 详细列出运行中的容器。
- `docker run`: 创建并启动新容器。
- `docker start/stop`: 启动/停止容器。
- `docker start/stop CONTAINERID`: 通过ID启动/停止容器。
- `docker start/stop MyWordPress`: 通过别名启动/停止容器。
- `docker inspect MyWordPress`: 查看容器详细信息。
- `docker logs MyWordPress`: 查看容器日志。
- `docker stats MyWordPress`: 查看容器资源使用。

### 容器内操作命令

- `docker exec 容器名 命令`: 在容器内执行命令。
- `docker exec -it 容器名 /bin/bash`: 连接到容器的bash会话。
