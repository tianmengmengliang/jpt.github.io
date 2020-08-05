
You can use address the [editor GitHub](https://mail-proxy04.beyondsoft.com/BYSAzure-Mail01/mail/jiapengtao.nsf?OpenDatabase) 
You can use address the [editor GitHub](https://e-cology.beyondsoft.com/login/Login.jsp?logintype=1) 

飞冰
https://ice.alibaba-inc.com/docs/guide/start

图片裁剪包
https://www.npmjs.com/package/react-image-crop

https://codesandbox.io/s/72py4jlll6?file=/src/index.js


## React16 - 为什么你不需要 getDerivedStateFromProps
https://www.jianshu.com/p/cafe8162b4a8
```
  static getDerivedStateFromProps 和 componentWillReceiveProps 的显著区别
  触发机制:
  - UNSAFE_componentWillReceiveProps(nextProps) 在组件接收到新的参数时被触发.
  
  - getDerivedStateFromProps(props, state) 会在每次组件渲染前被调用
  > getDerivedStateFromProps 会在每次组件被重新渲染前被调用, 这意味着无论是父组件的更新, props 的变化, 或是组件内部执行了 setState(), 它都会被调用. 
  
  工作方式:
   参数是组件接收到的新的 props , 用于比对新的 props 和原有的 props, 用户需要在函数体中调用 setState() 来更新组件数据.
   接收新的 props 和组件当前的状态数据. 必须返回一个对象或return null, 它将作为更新状态数据.
   
  为什么不应该使用 getDerivedStateFromProps:
   1. 充满了限制,很难用。 这个静态方法中, 除了两个默认的位置参数 nextProps 和 currentState 以外, 你无法访问任何组件上的数据.
   2. 会被频繁地触发。 组件调用了setState(), 或者接收的props发生了变化, 或是父组件的更新都会导致子组件上的getDerivedStateFromProps被触发.
   3. 使用getDerivedStateFromProps时, 必须添加很多逻辑判断语句来处理 props 上的更新和 state 上的更新, 避免意外地返回了一个 Updater 再次更新数据。
   
  参考
  生命周期函数: https://reactjs.org/docs/react-component.html
```

## 前端面试官都会问你什么？
https://www.jianshu.com/p/65f94024247a
```
  面试准备阶段
学习以及复习基础知识
这一定是第一步需要做的事情，先制定规划，然后按照这一条既定的规划去学习以及复习，可分为六部分去准备：

css部分
像css这一部分，面试必问，但是它的东西很杂很多，我不知道有多少人和我感觉一样：学习前端最难的是css，而不是js。
css这一部分，布局、实现一个什么样的形状、一些属性的使用等问的会多一些～

javascript部分
JavaScript部分，数据类型到一些隐式转换这些基础知识，看代码说输出，v8底层执行机制、垃圾回收、闭包、作用域、作用域链，原型、原型链，手写代码，如：防抖、节流、bind、call、apply等，深拷贝、浅拷贝，Event Queue、Event Loop，Promise、async、await等等等都是必须要会的知识点，但是我们在学习的过程中还是要灵活一些，去学习这些思想，而不是一味的去死记硬背～

webpack部分
这一部分是前端工程化的内容，还是有必要会的。浅一点说要会的就是一些基础配置以及优化配置，还有像plugin和loader的区别等，再深一点就是配置的原理、以及如何写一个loader或者plugin，然后应用这些东西实现什么样的需求

框架部分
前端的框架有很多，现在流行的两个就是vue和react，我的技术栈是react，所以我是以react去准备的面试，在react里面，经常问的比如：生命周期、关于生命周期为什么要废弃，什么是虚拟dom、diff算法思想以及key的作用、有key没key有什么区别，如何解析jsx，hooks的应用等

http
关于服务这一块，面试也是会经常问，http状态码所代表的含义，http与https的区别，http的三次握手以及四次挥手等

项目
面试离不开项目，所以对自己过往项目的理解尤为重要，上面的很多知识点其实也可以根据项目问很多

下面按上面的五部分分享面试题：

css部分
1、css中box-sizing的属性? 计算一个元素是总宽度和总高度的方式box-sizing: content-box/border-box/inherit;
2、一个元素居中的办法（不确定宽高的情况下如何用定位的办法实现）? position:absoulte; left:50%; tranfrom:tranlate(-50%, 0);
3、两栏布局，左侧固定，右侧自适应? 
4、如何理解BFC? 
5、清除浮动overflow:hidden的原理，为什么可以清除?  
6、了解postcss吗?
7、less和css的区别?
8、看代码
<style>
.classA { color:blue; }
.classB { color:red;}
</style>
<p class="classB classA">hello</p>
元素p内的文字最终什么颜色...
9、画一个三角形、扇形，将一个圆分为四部分，对角部分是相同颜色，相邻部分为不同颜色?
    width: 200px;
    height: 200px;
    content: " ";
    border-top: 50px solid #c3c315;
    border-right: 50px solid #5fe4f3;
    border-left: 50px solid #d41313;
    border-bottom: 50px solid #3be874;

JS部分
1、看代码说输出，会涉及到EventQueue、EventLoop，面向对象底层机制，闭包等
2、let、const区别
3、浅拷贝和深拷贝有什么区别，实现深拷贝
4、实现数组去重，new Set的数组去重和自己实现的哪个性能会更好
5、说出数组的方法，map和forEach有何区别
6、说一下跨域，jsonp的原理是什么？node中间件解决跨域问题的原理是什么？
7、Object.create实现了什么？传null得到的结果和普通对象有什么区别？
8、对prototype和proto的理解
9、call、apply和bind有何区别，手写实现call
10、替代es6中拓展运算符传参的方式
11、如何实现继承？class里面super是干嘛的
12、import和require的区别
13、对promise的考察，then链的应用
14、实现一个发布订阅，有订阅（on），发布（emit），一次订阅功能（once）
15、实现防抖节流，它们两个之间的区别是什么？
16、实现请求并发限制，具体为：封装一个函数，传递请求并发的个数为参数，实现对并发请求的限制
17、说说闭包以及垃圾回收机制
18、利用async和await如何处理异常事件
19、箭头函数和普通函数有什么区别？如果想改变箭头函数中绑定this怎么办？
20、原生js判断鼠标在一个有对角线矩形的位置

框架部分
1、react中key的作用，有key没key有什么区别，比较同一层级节点什么意思？
2、你对虚拟dom和diff算法的理解，实现render函数
3、父子组件之间传值的方式，组件间传值的方式
4、如何解析jsx
5、生命周期都有哪几种，分别是在什么阶段做哪些事情？为什么要废弃一些生命周期？
6、关于react的优化方法
7、绑定this的几种方式
8、对fiber的理解
9、setState是同步还是异步的
10、redux以及react-redux
11、对高阶组件的理解

webpack
1、你都用过哪些webpack的配置
2、在你的项目里面用过哪些优化
3、plugin和loader的区别
4、用过哪些loader、plugin

http部分
1、http与https的区别?
2、http握手的次数以及过程? https://zhuanlan.zhihu.com/p/103000747
3、http的几个状态码，比如：304、200、500、502、504等? 

项目
1、项目里面最经典的一个问题（好几家公司都问了这个）：在你的项目里面解决了什么样的难题
2、在你的项目里面如何做的登录
3、在你的项目里面，如何解决xss攻击? 
   跨站脚本攻击简称XSS，是一种代码注入攻击。过滤&&添加白名单。 https://www.freebuf.com/articles/web/185654.html
4、也有一些关于小程序项目的：

在小程序时候踩过哪些坑

小程序里面存在域的概念吗

5、还有上面说到的一些知识点会结合项目问一下
```

## 前端安全系列（一）：如何防止XSS攻击？
https://www.freebuf.com/articles/web/185654.html
```
 XSS攻击来源分为存储型、反射型和 DOM 型三种。
 预防存储型和反射型XSS攻击:
   1.改成纯前端渲染，把代码和数据分隔开。
   2.对 HTML 做充分转义。
   纯前端渲染还需注意避免 DOM型漏洞（例如 onload 事件和 href 中的 javascript:xxx 等，请参考下文”预防 DOM 型 XSS 攻击“部分）。
   
 预防 DOM型 XSS攻击:
   在使用 .innerHTML、.outerHTML、document.write() 时要特别小心，不要把不可信的数据作为 HTML 插到页面上，而应尽量使用 .textContent、.setAttribute() 等。
   如果用 Vue/React 技术栈，并且不使用 v-html/dangerouslySetInnerHTML 功能，就在前端 render 阶段避免 innerHTML、outerHTML 的 XSS 隐患。
   DOM 中的内联事件监听器，如 location、onclick、onerror、onload、onmouseover 等，<a> 标签的 href 属性，JavaScript的 eval()、setTimeout()、setInterval()等，都能把字符串作为代码运行。如果不可信的数据拼接到字符串中传递给这些 API，很容易产生安全隐患，请务必避免。
```
