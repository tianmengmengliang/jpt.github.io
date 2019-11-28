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
