# yangmengwen.github.io
前端分享

## 前端面试题分享
### 关于this
> 搞清楚this的指向首先要弄明白是谁调用了它（被哪个对象调用了）
```html
 var x = 10;
 function () {
  alert(this.x);
 }
```
> 这里this指向的是window对象
```html
var x = 10;
var b = {};
b.x = 1;
b.y = function() {
  alert(this.x);
}
b.y();
```
> 这里的this指的是b这个对象
### this与call、apply
> 通过call(),apply()可以改变this的指向
> call和apply的功能相似，区别就是参数的不同，call（对象，数值）,apply(对象，数组)
```html
var x = 1;
function test() {
  alert(this.x);
}
var o = new object();
o.x = 10;
o.m = test;
o.m.apply() // 0 this指向全局
o.m.apply(o) // 10 this指向o这个对象
```

