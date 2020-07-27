
```markdown
## 表单控件的默认值设置
无论任何控件一旦被表单函数包裹，其的默认值的设置都只能使用 initeValue来设置；自定义的表单子组件被表单函数包裹，子组件里的value属性就是父级设置initeValue在子组件里默认值可通过props.value获取。
```
## react项目中antd样式没生效的情况解决。
```markdown
    方式1. 在入口html里直接导入antd样式文件cdn。<link crossorigin="anonymous" integrity="sha384-5vwSfdTy/jvTtw6eQtXrrXmQP83ZwMMv4AL8Zhk8AwaPZ0/2RVyT01xnX9exaNOi" href="https://lib.baomitu.com/antd/4.4.2/antd.css" rel="stylesheet">
    方式2. 使用 :global{ }将需要修改的样式包裹起来。
    方式3. 将copy-webpack-plugin插件添加到您的webpack配置中。
```

## 高德地图
```markdown
  地图属性
```
https://lbs.amap.com/api/javascript-api/example/map/click-to-get-lnglat 鼠标点击-->采点

```markdown
  获取可视区域的坐标；并判断图层在不在区域内。
```
https://lbs.amap.com/api/javascript-api/example/map/limit-map-show-range 获取可视区域的坐标

https://lbs.amap.com/api/javascript-api/reference/map/?sug_index=1

https://lbs.amap.com/api/javascript-api/example/relationship-judgment/ringring 判断

```markdown
  勾划区域；并编辑。
```
https://lbs.amap.com/api/javascript-api/example/mouse-operate-map/mouse-draw-overlayers 删除

https://lbs.amap.com/api/javascript-api/example/overlayers/polygon-draw-and-edit 编辑

https://lbs.amap.com/api/javascript-api/example/overlayers/overlay-draw 绘制

https://lbs.amap.com/api/javascript-api/reference/plugin/#AMap.MouseTool 结束绘制

https://lbs.amap.com/faq/js-api/map-js-api/cover/43364/?sug_index=7 用鼠标工具绘制覆盖物，如何获取覆盖物的路径？

https://lbs.amap.com/faq/js-api/map-js-api/cover/43418/?sug_index=0 编辑多边形后如何获取多边形的路径？


```markdown
  勾划区域。
```
https://lbs.amap.com/api/javascript-api/example/overlayers/overlay-draw 绘制矢量图。
https://lbs.amap.com/api/javascript-api/guide/overlays/editable-vector-overlay/?sug_index=0 编辑矢量图
https://lbs.amap.com/api/javascript-api/example/overlayers/polygon-draw-and-edit 多边形编辑
