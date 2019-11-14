---
layout: post
title: MySQL表结构相关操作(笔记)
description: MySQL笔记，记记记背背背
tags: MySQL
---



### 修改字段

```mysql
ALTER TABLE table_name
ADD 字段名称 字段属性 [完整性约束条件] [FIRST|AFTER 字段名称]
DROP TABLE table_name
DROP COLUMN column_name
DROP column_name
```

### 修改字段默认值
```mysql
ALTER TABLE table_name
ALTER 字段名称 SET DEFAULT 默认值
ALTER 字段名称 DROP DEFAULT
```

### 修改字段类型、字段属性



```mysql
ALTER TABLE table_name
MODIFY 字段名称 字段类型 [字段属性] [FIRST|AFTER 字段名称] 
```

### 修改字段名称

```mysql
ALTER TABLE table_name
CHANGE 原字段名称 新字段名称 字段类型 字段属性 [FIRST|AFTER 字段名称]
```



### 修改主键

* 删除主键时，如果主键有 `AUTO_INCREMENT` 修饰，则必须先去除 `AUTO_INCREMENT` 修饰才能 drop 主键

```mysql
ALTER TABLE table_name
ADD PRIMARY KEY(字段名称)
DROP PRIMARY KEY
```

### 修改唯一索引

```mysql
ALTER TABLE table_name
DROP INDEX 索引名称/字段名称
ADD UNIQUE INDEX 索引名称
ADD UNIQUE KEY 索引名称
```

### 修改数据表名称

```mysql
ALTER TABLE table_name
RENAME TO new_name
RENAME AS new_name
```

