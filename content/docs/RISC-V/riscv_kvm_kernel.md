---
title: "riscv_kvm_kernel"
date: 2024-05-14T15:27:43+08:00
draft: false
weight: 5
---

## 描述
编译安装 kvm risc-v 源码

## 版本
ubuntu 20.04

## 从源码编译

### 安装依赖
```bash
```

### 下载源码
```bash
mkdir -p riscv
cd risc-v

git clone git@github.com:kvm-riscv/linux.git kvm_riscv_linux
cd kvm_riscv_linux

export ARCH=riscv
export CROSS_COMPILE=/root/riscv-gnu-toolchain/install/bin/riscv64-unknown-linux-gnu-

mkdir build-riscv64

make -C linux O=`pwd`/build-riscv64 defconfig
make -C linux O=`pwd`/build-riscv64 -j 3
```

### 编译
