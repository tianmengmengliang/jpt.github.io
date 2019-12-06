学习笔记
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Type

- Content-Type 
   在请求中 (如POST 或 PUT)，客户端告诉服务器实际发送的数据类型。
   在响应中，标头告诉客户端实际返回的内容的内容类型。
   
   ## application/x-www-form-urlencoded 和 application/json 区别：
application/json的数据格式: json字符串； application/x-www-form-urlencoded的数据格式：键值对，key-value。
application/json数据放在body中，application/x-www-form-urlencoded都可以。
## 表单提交时，请求头设置为application/x-www-form-urlencoded，POST和GET的区别：
GET: 浏览器用x-www-form-urlencoded的编码方式把form数据转换成一个字串（name1=value1&name2=value2…），然后把这个字串append到url后面，用?分割，加载这个新的url
POST: 浏览器把form数据封装到http body中，然后发送到server
## springmvc对application/x-www-form-urlencoded和application/json的处理：
application/x-www-form-urlencoded：get方式中queryString的值，和post方式中 body data的值都会被Servlet接受到并转化到Request.getParameter()参数集中，所以@RequestParam可以获取的到。
application/json：后端必须用@RequestBody接受，因为GET请求没有body所以无法接受，只能使用post方式。
