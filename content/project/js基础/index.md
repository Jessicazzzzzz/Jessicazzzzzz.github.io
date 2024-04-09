---
title: js基础学习
summary: An example of using the in-built project page.
tags:
  - js
date: '2024-04-09'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  focal_point: Smart

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

### 值传递和引用传递

- 值传递在存储在栈中,
- 引用传递首先是变量存储对象的地址,而这个地址是存储在堆中的

> 为什么这么处理?
> 这是从性能角度去考虑的,如果是值存储,直接copy,那么一般情况下,它的存储量比较下,如果存储大的话,我们就应该考虑引用类型

常见的值类型

- undefined 
- Symbol('s')
- string
- number
- boolean
  
常见的引用类型
```js
const obj ={x:100}
const arr = ['a','b','c']
const n = null // 特殊引用类型,指针指向为空地址
function fn(){}
```

### typeof 
- 识别所有的值类型
- 识别函数
- 判断是否是引用类型(不可再细分),它只能识别到 'object'

### 手写深拷贝
```js 
// 将一个对象里面的值全部拷贝到另一个对象中去
// 
function deepClone(obj={}){
// 判断类型,一定要使用typeof 来进行判断
if(typeof obj!=='object' || obj == null)return obj
 let res 
 // 确定返回类型是{} 还是[]
 // 需要用instanceof 
 if(res instanceof Array){
     res = []
 }else {
      res = {}
 }
 for(const key in obj){
 // hasOwnProperty 是用来判断obj 的这个属性是属于它自己的还是属于它父类的
  if(obj.hasOwnProperty(key)){
    // 正常来说,我们是这么赋值,但是如果obj[key]是个引用类型
    // 那么这个就不是copy 了
    // 那我们怎么处理呢
    // obj[key] 是什么类型,如果是值
    // res[key] = value ,如果是object ,那么就继续递归
   res[key] = deepClone(obj[key])
  }
 }
  return res 
}
```

### 类型转换
- 字符串拼接
- ==
	- 它会尽量的让它们转换类型去匹配是否相等
```js
	100 =='100'
	0==''
	0==false
	false==''
	null == undefined 
```
>  我们只要记住
>  除了== null 之外, 其他都一律用 === 
```js
const obj = {}
if(obj.a == null ){}
// 相当于
if(obj.a === null || obj.a === undefined)
```
- if语句和逻辑运算
	- truly 变量  !!var === true
	- falsely 变量  !!var === false
	```js
	// 其他情况都是true
	// 我们可以通过这个来进行if 条件的判断
	!!0 ===false 
	!!NaN ===false
	!!'' ===false
	!!null ===false
	!!undefined ===false
	!!false ===false
	
```