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

js中判断是什么类型的数据typeof
https://zhidao.baidu.com/question/2013766721575886428.html?fr=iks&word=Object.prototype.toString.call%28%29&ie=gbk
```markdown
如何判断js中的数据类型：typeof、instanceof、 constructor、 prototype方法比较
如何判断js中的类型呢，先举几个例子：
var a = "iamstring.";
var b = 222;
var c= [1,2,3];
var d = new Date();
var e = function(){alert(111);};
var f = function(){this.name="22";};
最常见的判断方法：typeof
alert(typeof a) ------------> string
alert(typeof b) ------------> number
alert(typeof c) ------------> object
alert(typeof d) ------------> object
alert(typeof e) ------------> function
alert(typeof f) ------------> function
其中typeof返回的类型都是字符串形式，需注意，例如：
alert(typeof a == "string") -------------> true
alert(typeof a == String) ---------------> false
另外typeof 可以判断function的类型；在判断除Object类型的对象时比较方便。
判断已知对象类型的方法： instanceof
alert(c instanceof Array) ---------------> true
alert(d instanceof Date)
alert(f instanceof Function) ------------> true
alert(f instanceof function) ------------> false
注意：instanceof 后面一定要是对象类型，并且大小写不能错，该方法适合一些条件选择或分支。
根据对象的constructor判断： constructor
alert(c.constructor === Array) ----------> true
alert(d.constructor === Date) -----------> true
alert(e.constructor === Function) -------> true
注意： constructor 在类继承时会出错
eg,
function A(){};
function B(){};
A.prototype = new B(); //A继承自B
var aObj = new A();
alert(aobj.constructor === B) -----------> true;
alert(aobj.constructor === A) -----------> false;
而instanceof方法不会出现该问题，对象直接继承和间接继承的都会报true：
alert(aobj instanceof B) ----------------> true;
alert(aobj instanceof B) ----------------> true;
言归正传，解决construtor的问题通常是让对象的constructor手动指向自己：
aobj.constructor = A; //将自己的类赋值给对象的constructor属性
alert(aobj.constructor === A) -----------> true;
alert(aobj.constructor === B) -----------> false; //基类不会报true了;
通用但很繁琐的方法： prototype
alert(Object.prototype.toString.call(a) === ‘[object String]’) -------> true;
alert(Object.prototype.toString.call(b) === ‘[object Number]’) -------> true;
alert(Object.prototype.toString.call(c) === ‘[object Array]’) -------> true;
alert(Object.prototype.toString.call(d) === ‘[object Date]’) -------> true;
alert(Object.prototype.toString.call(e) === ‘[object Function]’) -------> true;
alert(Object.prototype.toString.call(f) === ‘[object Function]’) -------> true;
大小写不能写错，比较麻烦，但胜在通用。
通常情况下用typeof 判断就可以了，遇到预知Object类型的情况可以选用instanceof或constructor方法，简单总结下，挖个坑，欢迎补充！
 22    评论 分享 举报收起
爆料百科大碗
2018-03-31
typeof算是最常见的了，使用它会返回一个字符串，适合函数对象和基本类型（js中的基本类型：number、string、boolean、null、undefined、object［对象］）的判断。

console.log("测试number:"+typeof 1);  console.log("测试string:"+typeof "str"); 

console.log("测试false:"+typeof false);  console.log("测试null:"+typeof null); 

console.log("测试undefined:"+typeof undefined);  console.log("测试Object:"+typeof new Object());  

console.log("测试Object:"+typeof new Array());  

console.log("看看typeof NaN是啥:"+typeof NaN); 

console.log("我想看看数组［1，2，3]类型:"+typeof [1,2,3]);  

console.log("看看function是啥:"+typeof function(){});
```

