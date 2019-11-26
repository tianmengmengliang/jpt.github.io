json格式化工具：  
https://www.json.cn/#


对象数组：   
https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype
```markdown
判断数组类型
Array.isArray(fruits); 返回布尔

function fun(){
}
Function.prototype.isPrototypeOf(fun);//true
Array.prototype.isPrototypeOf(fun);//false
Array.prototpye数组对象原型

Array.prototype.isPrototypeOf([]);//true
Array.prototype.isPrototypeOf(fun);//false
```
