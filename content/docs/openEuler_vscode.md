---
title: "OpenEuler_vscode"
date: 2023-06-20T15:27:43+08:00
draft: false
weight: 15
---

## 描述
安装完 openEuler 虚拟机后，通过 vscode remote-ssh 无法连接上


## 版本
openEuler 23.03

## 解决方法

进入 openEuler 23.03 vm 后，修改 /etc/ssh/sshd_config 配置

```shell
AllowAgentForwarding yes
AllowTcpForwarding yes
```

重启 ssh 服务
```shell
systemctl restart sshd.service
```
