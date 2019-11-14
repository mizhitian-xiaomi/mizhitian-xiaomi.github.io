---
layout: post
title: MySQL存储引擎 MyISAM & InnoDB(笔记)
description: MySQL笔记，记记记背背背
tags: MySQL
---

### MyISAM

* 默认产生
  * `.frm `  表结构文件 
  * `.myi  `  索引文件 
  * `.myd`  数据文件
* 在创建表的时候指定数据文件和索引文件的存储位置，只有 MyISAM 表支持
* 单表最大支持的数据量 `2^64` 条记录
* 每个表最多可以建立 `64` 个索引
* 每个复合索引最多包含 `16` 个列，索引值最大长度时 `1000B`
* MyISAM 引擎的存储格式：
  * 定长 (`FIXED静态`) 
    * 字段中不包含 `VARCHAR`/`TEXT`/`BLOB` 
    * 空间换时间
  * 动态 (`DYNAMIC`) 
    * 字段包含了 `VARCHAR`/`TEXT`/`BLOB` 
    * 占用空间小，处理复杂，时间换空间
  * 压缩 (`COMPRESSED`)

### InnoDB 

* 默认存储引擎
* 默认产生
  * `.frm`  表结构文件 
  * `.ibd`  数据和索引在表空间文件中
* 设计遵循 ACID 模型，拥有从服务崩溃中恢复的能力，最大限度保护用户数据
  * `Atomicity`   原子性
  * `Consistency` 一致性
  * `Isolation`   隔离性
  * `Durability`  持久性
* 行级锁，提升多用户并发是的读写性能
* 支持外键，保证数据的一致性和完整性
* 拥有自己独立的缓冲池，常用的数据和索引都在缓存中
* 对于 `DELETE` `UPDATE` `INSERT` 操作，使用一种 `change buffering` 的机制来自动优化，提供一致性的读，缓存变更的数据，减少磁盘I/O，提高性能
* 支持外键，保证数据的一致性和完整性
* 所有的表都需要创建主键，最好是配合上 `AUTO_INCREMENT`，也可以放到经常查询的列作为主键



> logging
>
> - 2019/11/14 xiaomi init