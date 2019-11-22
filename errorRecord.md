
### 报错记录
1. - 场景：列表页接口响应后，数据加载完成后，页面的静态资源请求全部变红(404),页面加载报错。
   - 解决：a.先将响应数据置空,页面不报错。b.响应数据回填组件时页面报错,就说明是数据的问题(检查发现table有一条数据是null)。

2. - Warning: Stateless function components cannot be given refs. Attempts to access this ref will fail.
   - 原因：Ref属性指向的节点`不能是函数组件`。
   - 解决：子组件（通过forwardRef方法创建）
   https://blog.csdn.net/liwusen/article/details/80009968
   
3. - Uncaught Error: Minified React error #44; visit https://reactjs.org/docs/error-decoder.html/?invariant=44   
   - 项目构建的框架react版本 和 项目中其他依赖的react版本不一致造成的。不不一致的版本依赖删掉，或都升级使用版本一致的react。
   
4. - 异步请求函数报错的问题。
   - uncaught at check call: argument fn is undefined；
   - Uncaught (in promise) Error: call: argument fn is undefined；？？？




