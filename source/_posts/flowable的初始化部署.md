---
title: flowable的初始化部署
date: 2024-08-08 09:49:27
tags: flowable
---
当我使用flowable7.0.1时，当时在tomcat部署时，使用的
```bash
.\catalina run
```
命令部署flowable。
使用下面命令验证一下
```bash
curl --user rest-admin:test http://localhost:8080/flowable-rest/service/management/engine
```
会返回404的错误，不是一个json字符串
![图1](1.png)

但我以为会是flowable版本问题，就换了个6.8.1(但应该跟这个没关系),而是直接使用tomcat启动命令
```bash
startup.bat
```
或 
```bash
startup.sh
```
我用的是startup.bat，就成功了
![图2](2.png)