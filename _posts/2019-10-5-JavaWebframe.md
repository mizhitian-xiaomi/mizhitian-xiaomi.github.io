---
layout: post
title: JavaWeb 三层框架
description: Javaweb理论
tags: JavaWeb
---



---

> 分工明确，降低耦合度，利于扩展项目

![javaweb 三层框架](https://raw.githubusercontent.com/mizhitian-xiaomi/mizhitian-xiaomi.github.io/master/images/posts/psb.png)



* **Web 层  -->  与 Web 相关的内容 (Servlet \ JSP \ Servlet相关API)**

* **业务层  -->  业务对象 (Service)**

  * 把零散的数据库操作集合在一起，成为一个`功能`

    > 比如一个转账功能，至少操作两次数据库，这些完成这一动作的所有零散操作的集合，是一个功能，一个业务

* **数据层  -->  操作数据库 DAO (Data Access Object)**

  * 对数据库进行零散的操作 -- 增删改查
  * 所有对 DAO 的操作度不能跳出 DAO 之外



> **refer**
>
> [av47001399](https://www.bilibili.com/video/av47001339/)

