### Node.js读取文件内容包括同步和异步两种方式。
```markdown
1、同步读取，调用的是readFileSync

var rf=require("fs");
var data=rf.readFileSync("test","utf-8");
console.log("step1:", data);
console.log("step2: END");
输出，先内容data，后end。

2、异步读取，调用readFile

var rf=require("fs");
rf.readFile("test",'utf-8',function(err,data){
    if(err){
        console.log("error");
    }else{
        console.log("step1:", data);
    }
});
console.log(step2: END");
输出，先end，后内容data。
```

```markdown
renderString(param1, data){
  this.validate(data, ()=> {
    // 在这里面写你要读文件结束后，要执行的代码。
     ......
     ......
     ......
  })
}

render(data){
  this.validate(data, ()=> {
    // 在这里面写你要读文件结束后，要执行的代码。
    .....
    .....
    .....
  })
}

validate(data, callback) {
  ....
  readlineObj.on('close', ()=>{
     ....
     console.log('读文件结束啦ok')
     // 执行回调函数
     callback()
  });
}
```
12月份前端学习
```markdown
 https://juejin.im/book/5c526902e51d4543805ef35e  你不知道的 Chrome调试技巧。
 https://juejin.im/post/59ab7b36f265da24934b2470#heading-2  函数绑定。
 
 继承，实现一个继承示例。
 原型链，
 继承链
 闭包原理。
 《javascript高级程序设计》  http、tcp通信。
```

原型与原型链的理解
https://www.jianshu.com/p/f30fa27999e3

我们希望构造函数中的某些属性是一个公共的属性，那么原型对象就登场了！给每一个构造函数都设置一个prototype属性，这个属性就指向原型对象。其实原型对象就只是个普通对象，里面存放着所有实例对象需要共享的属性和方法！所以，我们把需要共享的放到原型对象里，把不需要共享的属性和方法存在构造函数里！
[修改prototype属性会影响它的所有实例的sex的值！！](https://www.jianshu.com/p/f30fa27999e3)。 

yin构造函数就是实例对象的原型。 事实上，js里完全依靠"原型链"(prototype chain)模式来实现继承。
实现继承：proto会指向上一层的原型对象，而上一层的结构依然类似，那么就利用proto一直指向Object的原型对象上！`Object.prototype.__proto__ = null;` 表示到达最顶端。 如此形成了原型链继承。

JS实现继承的几种常用方式
https://www.jb51.net/article/163679.htm
