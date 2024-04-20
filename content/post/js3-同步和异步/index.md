---
title: 同步和异步
summary: 理解同步和异步
date: 2024-04-13
draft: false
featured: false
authors:
  - admin
  - Jess
tags:
  - js
categories:
  - 前端面试
---

### 同步和异步的区别
### 手写promise 加载一张图片
### 前端使用异步的场景


#### 单线程和异步 
> js 是单线程语言, 它只能同时做一件事, JS和DOM渲染共用同一个线程
> 那么遇到等待(网络请求,定时任务) 不能卡住 
> 所以需要异步,变相的可以同时执行多个任务
> 异步不会阻塞代码执行
> 同步会阻塞代码执行


### Promise 
> 解决了call back hell , 它是变成了一层的调用成功就可以then,失败就是catch

```js
const url = 'XXX'

  

function loadImg(url){

return new Promise((resolve,reject)=>{

const img = document.createElement('img')

img.src = url

img.onload = ()=>{

resolve(img)

}

img.onerror = ()=>{

reject('图片加载失败')

}

})

}

loadImg(url).then((img)=>{

console.log(img.width);

return img  // 这个返回值如果成功就会去调用下一个then

}).then((img)=>{

console.log(img.height);

}).catch((err)=>{

console.log(err);

})
```
[深入理解promise 参考](https://juejin.cn/post/7261252130442805285)

```js
class SelfPromise {

constructor(executor) {

this.status = 'pending'

this.value = undefined

this.reason = undefined

this.onResolvedCallback = []

this.onRejectedCallback = []

let resolve = (value) => {

if (this.status === 'pending') {

this.status = 'fulfilled'

this.value = value

this.onResolvedCallback.forEach(fn => fn())

}

}

let reject = (reason) => {

if (this.status === 'pending') {

this.status = 'rejected'

this.reason = reason

this.onRejectedCallback.forEach(fn => fn())

}

}

try {

executor(resolve, reject)

} catch (error) {

reject(error)

}

}

then(onFulfilled, onRejected) {

const promise2 = new SelfPromise((resolve, reject) => {

// 回调的值穿透

onFulfilled = typeof onFulfilled === 'function' ? onFulfilled : value => value

onRejected = typeof onRejected === 'function' ? onRejected : reason => { throw reason }

const fulfilledMicrotask = () => {

queueMicrotask(() => {

if(this.value && this.value.then === 'function'){

this.value.then(value=>{

const v = onFulfilled(value)

resolvePromise(promise2,v, resolve, reject)},error=>{

const v = onRejected(error)

resolvePromise(promise2,v, resolve, reject)

})

  

}else {

const v = onFulfilled(this.value)

resolvePromise(promise2,v, resolve, reject)

}

}

)

}

  

const rejectedMicrotask = () => {

queueMicrotask(() => {

const v = onRejected(this.reason)

resolvePromise(promise2,v, resolve, reject)

}

)

}

  

if (this.status === 'fulfilled') {

// const v = onFulfilled(this.value)

// resolvePromise(v, resolve, reject)

fulfilledMicrotask()

}

if (this.status === 'rejected') {

// const v = onRejected(this.reason)

// resolvePromise(v, resolve, reject)

rejectedMicrotask()

}

//这个是可以出来异步的

// 因为有setTimeout执行resolve,所以then 执行的时候, 状态还是pending

// 所以要把成功和失败的回调函数存起来

if (this.status === 'pending') {

this.onResolvedCallback.push(fulfilledMicrotask)

this.onRejectedCallback.push(rejectedMicrotask)

}

})

return promise2

}

}

  

function resolvePromise(promise2, value, resolve, reject) {

if(promise2 === value) {

return reject(new TypeError('Chaining cycle detected for promise'))

}

if(typeof value === 'object' || typeof value === 'function'){

if(value==null){

return resolve(value)

}

let called = false

const then = value.then

try{

// 如果返回值是Promise或者是thenable 对象

// 那么就交给它的then处理

if(typeof value.then === 'function'){

// 确保thenable可以异步执行

queueMicrotask(() => {

// 保持this指向是thenable 对象

then.call(value,(value2)=>{

if(called) return

called = true

resolvePromise(promise2, value2, resolve, reject)

},

(reason)=>{

if(called) return

called = true

reject(

reason

)

}

)

})

// value.then(resolve, reject)

}else{

resolve(value)

}

}catch(e){

if(called) return

called = true

reject(e)

}

  

}else{

resolve(value)

}

}

  

const p = new SelfPromise((resolve, reject) => {

setTimeout(() => {

resolve('fulfilled')

})

})

  

p.then(res => {

console.log("1" + res)

})

p.then(res => {

console.log("2" + res)

})

p.then(res => {

console.log("3" + res)

})

  

const p1 = new SelfPromise((resolve, reject) => {

resolve(1)

})

// then 回调,返回值是一个promise,那么下一个then回调的参数就是这个resolve 或者是 reject 函数传入的值

// 如果返回值是一个thenable，那么下一个then回调的参数就是这个thenable的resolve 或者是 reject 函数传入的值

// 如果是其他对象或者是原始数据的值,那么下一个then 回调的参数就是这个对象或者是原始数据的值

p1.then(res => {

console.log(res)

return new SelfPromise((resolve, reject) => {

resolve(2)

})

}).then(res => {

console.log(res)

})

  

const p2 = new SelfPromise((resolve, reject) => {

resolve(3)

})

const p3 = p2.then(res => {

console.log(res)

return p3

})

  

p3.then(res => {

console.log(2)

console.log("fulfilled",res);

}, reason => {

console.log(3);

console.log("rejected",reason);

})

  

const p4 = new SelfPromise((resolve, reject) => {

resolve(4)

})

// 测试穿透

p4.then().then().then(res => {

console.log(res)

})
```