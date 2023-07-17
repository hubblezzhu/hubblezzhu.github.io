---
title: "openEuler_redis"
date: 2023-07-12T14:35:57+08:00
draft: false
weight: 5
---


## 描述
openEuler启动redis



## docker 启动 redis server

拉取镜像
```bash
docker pull redis:latest
```

拉起 redis server docker
```bash
docker run -itd --name my_redis -p 6379:6379 --restart=always redis
```


## docker启动 memtier_benchmark
拉取镜像
```bash
docker pull redislabs/memtier_benchmark:latest

```

查看 help 信息
```bash
docker run --rm redislabs/memtier_benchmark:latest --help
```


打流
```bash
docker run --rm redislabs/memtier_benchmark:latest -s 192.168.101.222 -n 100000  -t 4 --ratio 1:0
```
