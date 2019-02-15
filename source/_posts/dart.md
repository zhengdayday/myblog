---
title: Dart基础
date: 2019-02-01 09:56:43
categories:
- Flutter
tags: 
- 教程
thumbnail: /img/one主题/康娜.gif
primarycolor: brown
accentcolor: blueGrey
---

本篇是学习Dart基础语法

## 搭建

```
export PUB_HOSTED_URL=https://pub.flutter-io.cn //国内用户需要设置
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn //国内用户需要设置
```

##语法

var可以定义变量

```dart

var tag = "666";

```

dart 中的number分为int和double,只有bool可以if(), dart的switch支持string

dart不需要给变量设置setter getter方法

dart final和const表示常量.　static const组合代表了静态常量．其中const的值在编译期确定，final需要到编译时才确定．


dart数组等于列表

```dart

var list = [];

List list = new List();
```

dart下?? ??=属于操作符

```dart

AA ?? "999";//如果AA为空,返回999;

AA ??= "999";//如果AA为空给AA设置为999

```

dart方法可以设置参数默认值和指定名称

dart可以用_下横线直接代表private，但是有@protected注解


dart中多构造函数，可以通过如下代码实现．默认的构造方法只能有一个而通过Model.empty()方法可以创建一个空参数的类．方法名称随意命名


```dart

class ModelA{
  
  String name;
  
  String tag;
  
  // 默认构造函数，赋值给name和tag
  ModelA(this.name, this.tag);
  
  // 返回一个空的ModelA
  ModelA.empty();
  
  // 返回一个设置了name的ModelA
  ModelA.forName(this.name);
  
}

```