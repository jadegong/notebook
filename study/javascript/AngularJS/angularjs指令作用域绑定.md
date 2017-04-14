# angularjs中指令作用域
[TOC]
angularjs中指令具有非常大的用途，很多DOM操作以及一些组件都可以通过指令来实现。指令中最难以搞清楚的是作用域绑定。
## scope关系
scope不同的定义表示的含义。
### 默认值false
angularjs指令中scope默认为false，表示指令与上一级公用一个作用域scope。在指令中可以轻松访问到父作用域中定义的变量。
### 赋值true
指令scope赋值为true时，表示指令作用域与父作用域隔离，但是指令scope会继承父作用域，也就是说父作用域改变会造成子作用域改变，子作用域改变则不会影响父作用域。
## 定义为一个对象{}
指令scope定义为一个对象时，表示指令scope与父作用域隔离，而且指令作用域不继承父作用域。也就是说两个作用域没有关系。
## scope为对象时的绑定
目前在开发过程中大部分指令作用域会使用上面第三种定义方式，也就是定义为一个对象{}，然而在实际使用中，指令依旧需要和父作用域进行交互，所以在定义scope中参数时，可以使用以下方法。
### @单向绑定

```js
scope : {
    attribute1: '@'
}
```
在指令中，如果定义的属性如上，那么表示父作用域中相同名称的属性单向绑定至指令的作用域中。
### =双向绑定
### &表达式或函数
## 参考文档
1: [指令<AngularJs> - Halower - 博客园](http://www.cnblogs.com/rohelm/p/4051437.html);
2: [Angular学习心得之directive——scope选项与绑定策略](https://my.oschina.net/u/2342955/blog/408889);
3: [AngularJS Directive 隔离 Scope 数据交互](https://blog.coding.net/blog/angularjs-directive-isolate-scope);