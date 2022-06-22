## html
1.常见单位：px、rem、em
2.rem和em的区别：rem是相对根元素的字体大小，em是相对父级元素大小
## CSS
1.postion定位几种：static\relative\absolute\fixed
2.relative和absolute区别：relative相对自身定位，absolute相对于离他最近的父级元素position不为static

## JS
1.数组常用方法：（哪些改变了原数组哪些不改变）
2.跨域相关（同源，影响，解决方法jsonp、cors(access-control-allow-origin)）
## HTTP
1.缓存：强缓存、协商缓存（expires、cache-control、last-modified\if-last-modified-since、Etag\if-Match）
## VUE
1.vue-router原理：hash\history;
2.路由守卫：next作用、异常处理

## 手写
1.手写sleep(500)
 实现await sleep(500);
console.log('wait 500ms');

```javascript
const sleep=(time)=>{
    return new Promise(resolve=>{
        setTimeout(resolve,time);
    })
}
```
2.输出（var,let,const区别，变量提升）      答案：报错  暂时性死区 
```javascript
var a = 3;
{
    console.log(a);
    let a = 4;
}
```
3.输出
```javascript
promise.then(succ, fail)//状态取决于succ和fail里面的结果，如果报错就rejected，如果正常就是resolved
promise.then(succ).catch(fail)//状态一定为resolved
```
4.手写 改写promise.all实现传入一个数组，返回值一定是resolved状态
```javascript
function allFinished(array){
    let arr=array.map(value=>{
       return value.catch(()=>{})
    });
    return Promise.all(arr);
}
```
