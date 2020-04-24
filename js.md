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
