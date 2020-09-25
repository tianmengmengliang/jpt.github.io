# 语法糖是什么？
https://www.zhihu.com/question/20651624
```markdown
  
```

编程题：

 JS数组reduce()方法详解及高级技巧
  https://www.jianshu.com/p/e375ba1cfc47
  
js连续赋值的问题：  https://blog.csdn.net/yjd19970908/article/details/80671426

前端系统复习之CSS盒模型： https://blog.csdn.net/m0_37585915/article/details/78501760

https://blog.csdn.net/xuehangongzi/article/details/80713786?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.edu_weight&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.edu_weight


JS判断值是否是数字
 ```markdown
    // isNaN()函数 把空串 空格 以及NUll 按照0来处理 所以用typeof先去除，
    // typeof判断 NaN 竟然是number类型。

    function isNum(value) {
        return typeof value === 'number' && !isNaN(value);
    }
 ```
清除input的历史记录
```markdown
    加上“autocomplete”属性，禁止历史的显示

    <input class="" type="text" autocomplete="off"></input>
```
css绘制三角形 https://www.jb51.net/css/640058.html
```markdown
    // 小三角
    div:after{
      position: absolute;
      width: 0px;
      height: 0px;
      content: " ";
      border-top: 100px solid #ff0;
      border-right: 100px solid transparent;
      border-left: 100px solid transparent;
    }
    // 四色板
    div:after{
      position: absolute;
      width: 250px;
      height: 250px;
      content: " ";
      border-top: 100px solid #ff0;
      border-right: 100px solid #f00;
      border-left: 100px solid  #f60;
      border-bottom: 100px solid #4f0;
    }
```
js截取字符串的三个方法 substring()、substr()、slice()
https://segmentfault.com/a/1190000016387899
``` 
   常使用的截取方法为substr()
```

数据统计页面遇到的处理。
  百分比处理：占比项的最后一项的值计算方式为 1减其他各项和。
  当页面展示的数值比较长时占据的空间多的情况，可以通过调整字体大小。
  
Moment.js进行时间类型转换  https://blog.csdn.net/u011646268/article/details/73863524

深拷贝 https://www.jianshu.com/p/55d3e1b3afab
```markdown
    1.浅拷贝
    b复制了a，修改a，b也跟着变。
    
    基本数据类型有哪些，number,string,boolean,null,undefined五类。
    引用数据类型(Object类)有常规名值对的 无序对象{a:1}，数组[1,2,3]，以及函数等。

    当b=a进行拷贝时，其实复制的是a的引用地址，而非堆里面的值。
    要是在堆内存中也开辟一个新的内存专门为b存放值，就像基本类型那样，就达到深拷贝的效果了。
    2. 实现深拷贝
    递归递归去复制所有层级属性。
    还可以借用 JSON.stringify(obj)和JSON.parse(obj)
    
```

e.preventDefault()是阻止默认行为啊！！
a元素的默认行为点击会跳转。

想要在异步函数中继续使event属性可访问，需要使用event.persist()事件，这将从池中删除综合事件，并允许用户代码保留对该事件的引用。
https://www.cnblogs.com/lyraLee/p/11577511.html

### 将参数传递给事件处理程序
```markdown
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
function deleteRow(id, event) {
  event.persist();
  const type = event.type;
}

<button onClick={deleteRow(id)}>Delete Row</button>
function deleteRow(id, event) {
  return function() {
    console.log(id);
  }
}
```
js中函数不会自己绑定的，函数传参时：
1. 使用箭头函数。
2. bind()
3. 返回一个匿名函数。


  ## 动态生成决策树
  https://www.cnblogs.com/hess/p/6626226.html
![image](https://images2015.cnblogs.com/blog/982312/201703/982312-20170327130533686-1341123924.gif)

 ## js 获取页面滚动事件及滚动距离
 - [js-监听页面滚动](https://www.cnblogs.com/liuqingxia/p/10694101.html)
 - [js 获取浏览器页面滚动的高度](https://www.cnblogs.com/pumushan/p/4969104.html)
 
 获取元素在页面中位置
 ```js
  // 1.通过元素的offsetLeft和offsetTop
  var domObj = docunment.getElementById('dom');
  domObj.offsetLeft; //10
  domObj.offsetTop; //10
 ```
 - [js获取元素的滚动高度，和距离顶部的高度](https://www.cnblogs.com/wangyihong/p/8056859.html)

## 前端如何解决跨域的问题？
https://blog.csdn.net/weixin_30929195/article/details/97796143?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-3.edu_weight&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-3.edu_weight
跨域的问题由浏览器拦截了请求造成的。 浏览器根据预检请求的响应头里的信息判断是否跨域，跨域了则拦截请求。 解决跨域img、script这些标签是不受同源策略限制，但仅限get请求方式，post请求没办法的。

## iframe无法嵌入页面的问题。
https://blog.csdn.net/chenyanggo/article/details/77946360

## 抽象语法树AST，中的type表示什么呢？
 type 表达当前块的类型。 https://blog.csdn.net/weixin_44135121/article/details/104161823?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.edu_weight&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.edu_weight

 代码转 抽象语法树的在线演示：https://resources.jointjs.com/demos/javascript-ast


## 面试题：彻底弄懂函数防抖和节流
https://blog.csdn.net/chenxi_li/article/details/101100467?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.edu_weight&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.edu_weight

> 在事件被触发n秒后再执行回调，如果在这n秒内又被触发，则重新计时。
> 函数节流的目的，是为了限制函数一段时间内能执行的次数。

```markdown
   1. 循环引用的对象使用 JSON.stringify 为什么会报错?
   https://www.cnblogs.com/zhangguicheng/p/12173538.html
```
