## Welcome to GitHub Pages

css3 实现左右布局: `主要用于券布局`
https://blog.csdn.net/qq_40190624/article/details/89463203
https://blog.csdn.net/weixin_38606332/article/details/80868138
  ```markdown
    div.parent{
      display:flex;
    }
    div.child{
      margin:auto;
    }
  ```
将div均分为三等份:
 ```markdown
    1. .parent: { display: table;} .son { display: table-cell;}
       
    2. .parent: { display: flex;} .son { flex: 1;}
  ```
https://my.oschina.net/u/266531/blog/795080
https://blog.csdn.net/weixin_38606332/article/details/80868138

## :first-child  :last-child  :only-child  :nth-child  
- 子代选择符【CSS选择符】：https://www.jianshu.com/p/59d1f60ff74a
- 所有CSS伪类/元素【所有CSS伪类/伪元素】: https://www.runoob.com/css/css-pseudo-classes.html
   ```markdown
    :nth-child(n) 选择器匹配父元素中的第n个子元素
    
    伪类:, 伪元素:, 除了selection
   ```
- 子元素选择器 >。
## flex布局实现div子元素居两边
   ```markdown
    .parent: {
      display: flex;
      justify-content: space-between;
      align-items: center;
     }
   ```
## flex布局实现div子元素居中
   ```markdown
    方法1.
    .parent: {
      display: flex;
      justify-content: center; // 水平
      align-items: center; // 上下
     }
     
     方法2.使用百分比定位居中（地图组件里的关联度级别刻度条）
     .div {
       position: absolute;
       left: 50%;
       transform: translate(-50%, 0);
     }
   ```


## 内容撑开宽度
div{  width:auto; display:inline-block; }
## 内容撑开高度
div{  height:auto !important;  min-height:400px;  max-height:xxxpx; }

## css3中 百分比减固定宽度 https://www.cnblogs.com/ghfjj/p/7436597.html
   ```markdown
    div{ 
     /*实现了宽度为父容器宽度减去固定的300像素*/ 
     width: -webkit-calc(100% - 300px); 
     width: -moz-calc(100% - 300px); 
     width: calc(100% - 300px);
    }
   ```

## inline-block 左右元素上下不对齐的问题。
   ```markdown
     1.设置了属性 display：inline-block，是基于baseline对齐的，同一行的元素高度不同，会导致上下不齐。
     常用解决方案：
      添加 vertical-align属性，如 vertical-align: top|center; // 居顶|居中对齐。
      
     2.设置了属性 display：inline-block， 左右有间隔。是因为换行符的存在；归类为幽灵元素问题。
   ```

## flex 布局
   ```markdown
    display: flex;
    flex-direction: row/column; //布局方向水平排列/竖直排列。
    flex-wrap: nowrap/wrap; //换行/不换行。

    flex-shrink：0; 属性指定了flex元素的收缩规则。子元素们的宽度之和大于容器宽度的时候才会发生收缩，其收缩的大小是依据 flex-shrink 的值。
      注意：如果元素不是弹性盒对象的元素，则该属性不起作用。设置flex-shrink:0的元素不收缩，其他元素会受到挤压。
    flex-grow: 1; 属性用于设置或检索弹性盒子的扩展比率，占满剩余空间
    align-items: center/baseline; 上下方向对齐方式/项目的文字的基线对齐。。如：金额¥和价格底部轴线对齐。
    justify-content: flex-start/flex-end/center/space-between/space-around；水平(左右两边)方向的对齐方式。
    flex-flow: row wrap; 排列方向，且在必要的时候进行拆行。
  ```

  文本换行省略号 https://jingyan.baidu.com/article/f54ae2fc7ee91e1e92b8498f.html
  ```markdown
    overflow: hidden;
    text-overflow: ellipsis; 
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    这里要注意不要给标签添加高度，让文字自动撑开多行就行
  ```
  ```markdown
    演示方向到右下角的背景色线性渐变:
    #grad {
      background-image: linear-gradient(to right bottom, red , yellow);
    }
  ```

### rotate()存在兼容问题ios上图片出不来。 
https://juejin.im/post/5d5f449ef265da03a6531f41
父元素：transform: perspective(400); // 给父级添加这个属性。
子元素：transform: rotate(180);

## 深入研究 -webkit-overflow-scrolling: touch;移动端及ios页面上下滑动。
https://www.cnblogs.com/xiahj/p/8036419.html#1--webkit-overflow-scrollingtouch%E6%98%AF%E4%BB%80%E4%B9%88%EF%BC%9F


### Cursor:url()自定义鼠标指针样式为图片及图片的偏移量
https://developer.mozilla.org/zh-CN/docs/Web/CSS/cursor
  ```css
/* 关键字值 */
cursor: pointer;
cursor: auto;

/* 使用URL，提供一个关键字值作为备用 */
cursor: url(hand.cur), pointer;

/*  xy的坐标偏移值，最后提供一个关键字值作为备用 */
cursor:  url(cursor1.png) 4 12, auto;
cursor:  url(cursor2.png) 2 2, pointer;
  ```

## css 线性渐变
https://www.jianshu.com/p/1a67ef7b2417
  ```css
   <style>
#grad1 {
  height: 500px;
  background-image: linear-gradient(-50deg, #FF6219 20px, #FFEAE7 100% 100%);
}
</style>
  ```
## css中的空白元素、幽灵元素占据空间的问题
   原因：继承了父级css样式。
   空白元素继承了父级css属性：父级样式 font-size, line-height都设置为0，这样阻断其继承。

## css阻止文本选中 和 改变默认选中颜色
   ```css
    -webkit-user-select: none;
       -moz-user-select: none;
        -ms-user-select: none;
             user-select: none;
             
     ::selection {
          background:#d3d3d3; 
          color:#555;
      }        
   ```
## :before和::before的区别
二者写法是等效的，都表示伪元素。
- :before是CSS2的写法，::before是CSS3的写法。
- :before的兼容性比::before兼容性好，但是H5开发中建议使用::before
- 注意：
 伪元素要配合content属性一起使用   
