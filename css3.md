## Welcome to GitHub Pages

css3 实现左右布局: `主要用于券布局`
https://blog.csdn.net/qq_40190624/article/details/89463203
https://blog.csdn.net/weixin_38606332/article/details/80868138
```markdown
  1. display: table;  display: table-cell;
  2. display: flex;  flex: 1;
```

将div均分为三等份:
https://my.oschina.net/u/266531/blog/795080
https://blog.csdn.net/weixin_38606332/article/details/80868138

## :first-child  :last-child  :only-child  :nth-child  
- 子代选择符【CSS选择符】：https://www.jianshu.com/p/59d1f60ff74a
- 所有CSS伪类/元素【所有CSS伪类/伪元素】: https://www.runoob.com/css/css-pseudo-classes.html
   ```markdown
    :nth-child(n) 选择器匹配父元素中的第 n 个子元素
   ```
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
       transfrom: translate(-50%, 0);
     }
   ```


## 内容撑开宽度
div{  width:auto;  display:inline-block !important;  display:inline; }
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

## display:inline-block 左右元素上下不对齐的场景
   ```markdown
     解决办法：应用inline-block的元素加上 vertical-align: top; 
    .CSSElement {
      display: inline-block;
      vertical-align: top;
    }
   ```
