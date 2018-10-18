---
title: Neo4j概述
date: 2018-10-18 10:43:20
categories:
- Neo4j
tags: 
- 教程
thumbnail: /img/js异步和网络api发展史/cover.jpg
primarycolor: brown
accentcolor: blueGrey
---

本篇是学习Neo4j权威指南的第二篇

## Neo4j概述

Neo4j是由Java实现的开源的NoSQL图数据库

## 免索引邻接

用来保证关系查询的速度，数据库中的每个节点都会维护与它相邻节点的引用。因此每个节点都相当于与他相邻节点的微索引。
查询时间和图的整体规模无关，只与它附近节点的数量成正比。
