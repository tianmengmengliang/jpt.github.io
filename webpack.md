

## process.env.NODE_ENV 的作用
通过判断这个[变量](https://www.cnblogs.com/usebtf/p/9912413.html)区分开发环境或生产环境。
```markdown
- process.env.NODE_ENV 的作用。
 通过判断这个变量区分开发环境或生产环境

- 如何设置 process.env.NODE_ENV。
```

### url-loader | 将小图片url转base64字串的时，对图片大小限制
[A loader for webpack which transforms files into base64 URIs.](https://webpack.docschina.org/loaders/url-loader/#limit)


### 在react中使用 @符号导入模块
https://www.jianshu.com/p/f489cce2e7f1

eslint校验问题解决：Unable to resolve path to module '@/xxxx'.eslint(import/no-unresolved)
https://blog.csdn.net/weixin_34151004/article/details/91854509

## nvm（windows版本）对node版本管理。
nvm（windows版本）：https://github.com/coreybutler/nvm-windows
阿里出的tnvm: https://github.com/aliyun-node/tnvm

## npm平台
免费注册一个账号，发布自 己的公共包和私有包供其他人使用。 https://www.npmjs.com/
```markdown
    常用命令
    安装依赖包：npm i packageName --save（简写npm i packageName -S）
    安装某版本的包：npm i packageName@x.x.x --save
    希望写到开发依赖中：npm i packageName --save-dev（简写npm i packageName -D）
    删除某个NPM包使用：npm uninstall packageName
    
    安装tnpm
    npm install -g tnpm --registry=http://registry.npm.alibaba-inc.com
    
    使用下面的命令可以安装cnpm包
    npm install -g cnpm --registry=https://registry.npm.taobao.org
    
    npm scripts用于执行脚本, 文件中可以添加scripts字段.
```

## 安装Webpack-cli
```markdown
    npm install webpack-cli --save-dev
```
> Tips:这里建议在项目中安装 webpack-cli 并且使用 --save-dev 的配置将 webpack-cli 放到开发依赖中。

### 重学webpack配置
1. webpack基本配置属性说明。 https://segmentfault.com/a/1190000019923659
2. 掘金站内 webpack 优秀文章汇总。 https://blog.csdn.net/sinat_17775997/article/details/103652370
3. 从零配置webpack 4+react脚手架（一）https://juejin.im/post/5da5748851882555a8430641
4. Webpack刷题神器 https://juejin.im/post/5f0eb0405188252e4839bd5d

