---
title: Neo4j基础入门
date: 2018-10-18 15:07:08
categories:
- Neo4j
tags: 
- 教程
thumbnail: /img/one主题/cover.jpg
primarycolor: brown
accentcolor: blueGrey
---

本篇是学习Neo4j权威指南的第三篇

## 官网下载Neo4j桌面版本或者压缩包

* 桌面版本安装后，add一个Graph，然后选择对应的版本号，就可以用了。

* 压缩包解压即可用了

* cd进入到bin目录

* `neo4j console` 打开Neo4j控制台

* `neo4j start` 启动Neo4j

* `neo4j stop` 停止Neo4j

* `neo4j restart` 重启Neo4j

* `neo4j status` 查看Neo4j运行状态

* `neo4j install-service` 安装Neo4j在windows系统上的服务。

* `neo4j uninstall-service` 卸载Neo4j在windows系统上的服务。

* 启动后可以访问`http://localhost:7474/` 可以看到Neo4j的操作界面

* 默认的用户名和密码是neo4j

## Neo4j 图数据中基本元素与概念

节点(node)是图数据库中的一个基本元素， 用以表示一个实体记录，就像关系数据库中的一条记录一样。在Neo4j中节点可以包含多个属性(Property)和多个标签。

关系(relationship)同样是图数据库中的基本元素，当数据库中已经存在节点后，需要将节点连接起来构成图。关系就是用来连接两个节点。关系也成为图论的edge。关系起始和结束都是节点，关系只能有一个类型。
  
属性是由键值对组成，就像Java的哈希表一样，属性名类似变量名， 属性值类似变量值。不能为null
  
## 遍历 (Traversal)
Neo4j提供了一套高效的遍历API，可以指定遍历规则，然后让Neo4j自动按照遍历规则遍历并返回遍历的结果。遍历规则可以是广度优先搜索，也可以是深度优先搜索。

## 批量导入工具的使用

目前主要有两种导入Neo4j的工具

* `load csv` 指令

* `load csv from "file-url" as line return count(*)` 查看前csv文件行数

* `load csv from "file-rul" as line with lien return line limit 5` 查看前五行

* `load csv with headers from 'file-url as line with line return line limit 5` 并带有头部数据  

* `ne4j-import`工具, 后者目前放入了`neo4j-admin` 中 位于`bin`目录下，以上两种都是基于csv的

* `bin/neo4j-import --into retail.db --id-type string --nodes:Customer customer.csv --nodes products.csv --nodes:order_header.csv,orders1.csv,orders2.csv -- relationships:CONTAINS order_details.csv --relationships:ORDERD customer_orders_header.csv,orders1.csv,orders2.csv`

* `--nodes:`自居开头的csv文件是节点的csv文件，以`--relationships:`开头的是关系CSV文件；`--into`子句指明了导入Neo4j数据库的名称；`--id-type` 表示生成节点、关系主键类型为string类型

* neo4j-import不能使用Cypher语句

本系列的下一篇文章 - Neo4j之Cypher
