---
layout: post
title: "JavaScript的原型与对象"
date: 2015-03-02 11:17:43 +0800
comments: true
categories: JavaScript 技术
---
与许多面向对象的语言一样，JavaScript支持集成，即通过动态代理机制重用代码或数据。但不想许多传统语言，JavaScript的继承机制基于原型，而不是类。对于许多程序员来说，JavaScript是第一个不需要类实现面向对象的语言。尽管JavaScript使用了很多传统的面向对象语言的概念，但使用原型与使用类有很大差异。

####理解prototype、getPrototypeOf和\_\_proto\_\_之间的不同
* Obj.prototype 用于建立由new Obj()创建的对象的原型
* Object.getPrototypeOf(obj) 是ES5中用来获取obj对象的原型对象的标准方法
* obj.\_\_proto\_\_ 是获取obj对象的原型对象的非标准方法

可以使用prototype属性为对象增加或修改类属性或类方法。
	{}.prototype.print = function() {
console.log('print method');
}
