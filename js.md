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

