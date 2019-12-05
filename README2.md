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
