---
title: 原型和原型链
summary: 理解原型和原型链
tags:
  - js
date: '2024-04-13'
---
> 如何准确判断一个变量是不是数组
> class 原型本质,怎么理解


### class 和继承
-  constructor 
-  属性
- 方法
>  instanceof  用来判断是否是一个class 对象创建出来的
```js
class A {}
class B extends A {}
const c = new B()
c instanceof A //true
c instanceof B //true
c instanceof Object //true

```



#### 继承
- extends 
- 子类调用父类构造方法,需要用super()

### 类型判断和 instanceof 

### 原型和原型链
- class 创建出来的对象 typeof 是函数
-  __proto__ 显示原型
- Class.prototype 隐式原型

![](prototype.png)