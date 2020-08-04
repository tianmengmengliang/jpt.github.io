
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
