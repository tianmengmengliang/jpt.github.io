

componentDidUpdate() || didUpdate() 使用这些生命周期函数时注意一定要加if判断，不然会产生死循环导致内存泄露。
https://react.docschina.org/docs/react-component.html


getDerivedStateFromProps是一个静态函数，这个函数不能通过this访问到class的属性，也并不推荐直接访问属性。而是应该通过参数提供的nextProps以及prevState来进行判断，根据新传入的props来映射到state。需要注意的是，如果props传入的内容不需要影响到你的state，那么就需要返回一个null，这个返回值是必须的。


- componentWillReceiveProps性能问题。当外部多个属性在很短的时间间隔之内多次变化，就会导致componentWillReceiveProps被多次调用。这个调用并不会被合并，如果这次内容都会触发异步请求，那么可能会导致多个异步请求阻塞。
- 在使用getDerivedStateFromProps的时候，遇到了上面说的props在很短的时间内多次变化，也只会触发一次render，也就是只触发一次getDerivedStateFromProps。这样的优点。


## 使用 PropTypes进行类型检查
https://www.jianshu.com/p/2896acb5746b
```js
  MyComponent.propTypes = {
    //你可以定义一个属性是特定的JS类型（Array,Boolean,Function,Number,Object,String,Symbol）。默认情况下，这些都是可选的。
    optionalArray: PropTypes.array,
    optionalBool: PropTypes.bool,
    optionalFunc: PropTypes.func,
    optionalNumber: PropTypes.number,
    optionalObject: PropTypes.object,
    optionalString: PropTypes.string,
    optionalSymbol: PropTypes.symbol,

    //指定枚举类型：你可以把属性限制在某些特定值之内
    optionalEnum: PropTypes.oneOf(['News1', 'News2', 'News3']),

    // 指定多个类型：你也可以把属性类型限制在某些指定的类型范围内
    optionalUnion: PropTypes.oneOfType([
      PropTypes.string,
      PropTypes.number,
      PropTypes.instanceOf(Message)
    ]),
  }
```
## react项目本地运行正常，线上报错，引用的某依赖包和项目框架包react版本不一致的问题。
1. 将版本不一致的依赖包全部干掉。
2. 项目迁移。
