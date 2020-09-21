学习笔记
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Type

- Content-Type 
   在请求中 (如POST 或 PUT)，客户端告诉服务器实际发送的数据类型。
   在响应中，标头告诉客户端实际返回的内容的内容类型。
   
   ## application/x-www-form-urlencoded 和 application/json 区别：
   ```markdown
   application/json的数据格式: json字符串； application/x-www-form-urlencoded的数据格式：键值对，key-value。
   application/json数据放在body中，application/x-www-form-urlencoded都可以。
   ```
   ## 表单提交时，请求头设置为application/x-www-form-urlencoded，POST和GET的区别：
   ```markdown
   GET: 浏览器用x-www-form-urlencoded的编码方式把form数据转换成一个字串（name1=value1&name2=value2…），然后把这个字串append到url后面，用?分割，加载这个新的url。
   POST: 浏览器把form数据封装到http body中，然后发送到server。
   
   若符合下列任一情况，则用POST方法：
   * 请求的结果有持续性的副作用，例如，数据库内添加新的数据行。
   * 若使用GET方法，则表单上收集的数据可能让URL过长。
   * 要传送的数据不是采用7位的ASCII编码。

   若符合下列任一情况，则用GET方法：
   * 请求是为了查找资源，HTML表单数据仅用来帮助搜索。
   * 请求结果无持续性的副作用。
   * 收集的数据及HTML表单内的输入字段名称的总长不超过1024个字符。
   ```
   ## springmvc对application/x-www-form-urlencoded和application/json的处理：
   ```markdown
   application/x-www-form-urlencoded：get方式中queryString的值，和post方式中 body data的值都会被Servlet接受到并转化到Request.getParameter()参数集中，所以@RequestParam可以获取的到。
   application/json：后端必须用@RequestBody接受，因为GET请求没有body所以无法接受，只能使用post方式。
   ```

## 响应状态码：
```
  302 暂时重定向。服务端设置。
  403 forbidden。 比如图片资源，通过referrer值判断请求是否来自本站，若不是来自本站则返回403。
  解决方法：就是把referrer设置成no-referrer，请求不会带上referrer信息，对方服务器也就无法拦截了。
```
## 为什么http请求要３次握手与４次挥手？
https://www.zhihu.com/question/67772889
```
  HTTP本身是应用层协议，应用层本身并不约束数据传输层用的啥。
  如果传输层并不是 TCP/IP ，那就不一定有三次握手什么的。
  3次握手4次挥手是针对TCP连接来说的
  3次握手: 用来保障通讯双方,有通信的基础。
  4次挥手: 用来保障通讯双方,可以安全的回收TCP通信的系统资源。  
```
> HTTP访问控制（CORS）
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Access_control_CORS

> 前端面试之旅
https://juejin.im/post/6844903889653760007
