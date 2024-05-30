---
title: "riscv_qemu"
date: 2024-05-14T15:27:43+08:00
draft: false
weight: 5
---

## 描述
构建 qemu


## 版本
ubuntu 20.04

## 从源码编译

### 安装依赖
```bash
apt-get install python3-venv -y
apt-get install python3-pip -y


python3 -m pip install sphinx -y
python3 -m pip install sphinx_rtd_theme -y
python3 -m pip install ninja -y

```


### 下载源码


```bash
# 以 qemu 9.0 版本为例
wget https://mirrors.aliyun.com/blfs/conglomeration/qemu/qemu-9.0.0.tar.xz

tar -xvJf qemu-9.0.0.tar.xz

```

### 编译
```bash

cd qemu-9.0.0
# ../configure
./configure --enable-kvm --enable-virtfs --enable-slirp --target-list=riscv64-linux-user,riscv64-softmmu

make -j 15

```