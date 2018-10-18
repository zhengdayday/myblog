---
title: Neo4j之Cypher
date: 2018-10-18 16:20:43
categories:
- Neo4j
tags: 
- 教程
thumbnail: /img/one主题/康娜.gif
primarycolor: brown
accentcolor: blueGrey
---

本篇是学习Neo4j权威指南的第四篇

## Cypher是什么

Cypher是一种声明式图数据库查询语言，可以高效的查询和更新图数据。

Cypher借鉴了SQL语言的结构--查询可由各种各样的语句组合。语句被链接在一起，相互传递中间结果集。

## 模式(Pattern)

节点类似mysql的表，节点的标签类似mysql不同表面，节点的属性类似mysql一列，一个节点的数据类似mysql表的一行数据，拥有相同标签的节点通常具有类似的属性。

模式可以将很多节点和关系编码为任意复杂的想法。

## 节点语法

Cypher采用一对圆括号来表示节点， 如`()、(foo)` 下面是一些常见的节点表示法:

```
()
(matrix)
(:Movie)
(matrix:Movie)
(matrix:Movie {title:"the Matrix"})
(matrix:Movie {title:"the matrix", released:1997})
```

简单的()表达了一个匿名节点。如果想在其他地方引用这个节点，可以添加要给变量，如(matrix)。此变量的可见范围局限于单个语句。

Movie标签声明了节点的类型。Neo4j节点索引也会使用到标签，每个索引都是建立在一个标签和属性的组合上。节点的属性以key/value列表的形式存在，并外加一对大括号。
