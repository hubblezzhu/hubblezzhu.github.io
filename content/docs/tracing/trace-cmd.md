---
title: "trace-cmd"
date: 2023-07-14T15:17:47+08:00
draft: false
---

## 描述
trace-cmd 使用


## 环境

openEuler23_03 6.1.19-7.0.0.17.oe2303.aarch64

## 安装

```bash
dnf install trace-cmd -y
```


## 使用

#### 列出可用的 tracer
```bash
trace-cmd list -t
```
#### 列出可追踪的 function
```bash
trace-cmd list -f
```

#### 追踪特定函数
1、开始记录
```bash
trace-cmd record -P 281760 -p function_graph -l do_sys_open
```

2、查看结果
```bash
trace-cmd report
```
