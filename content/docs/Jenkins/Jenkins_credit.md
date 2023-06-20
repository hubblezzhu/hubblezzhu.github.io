---
title: "Jenkins_credit"
date: 2023-06-20T17:31:39+08:00
draft: false
---

## 描述

通过 jenkins script console 获取所有 jenkins 账号，密码


## 步骤

jenkins HOME 页面 -> manage jenkins -> script console

运行
```shell
com.cloudbees.plugins.credentials.SystemCredentialsProvider.getInstance().getCredentials().forEach{
  it.properties.each { prop, val ->
    println(prop + ' = "' + val + '"')
  }
  println("-----------------------")
}
```
