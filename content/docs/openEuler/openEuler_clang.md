---
title: "OpenEuler_clang"
date: 2023-06-27T14:08:00+08:00
draft: false
---

## 描述
openEuler 安装 clang



## 版本
openEuler： openEuler 23.03     \
clang    ： clang15             \
llvm     ： llvm15

## 步骤

```shell
dnf install clang15 llvm15 -y
```

```shell
export PATH=$PATH:/usr/lib64/llvm15/bin
```
