---
title: "openEuler_cgroup_v2"
date: 2023-06-27T15:55:46+08:00
draft: false
weight: 5
---

## 描述
openEuler 切换 cgroup v2



## 版本
openEuler： openEuler 23.03 x86

## 步骤

```shell
grubby --update-kernel=ALL --args=systemd.unified_cgroup_hierarchy=1
reboot

```
