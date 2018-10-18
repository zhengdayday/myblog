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
  
  属性是由键值对