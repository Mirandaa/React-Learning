## React 学习笔记

### 0. 搭建脚手架

在已下载node环境，并且node版本6.0+和npm版本5.2+的前提下，使用npx命令构建项目并运行

```shell
// install create-react-app
npm install create-react-app -g

// create a new react project
npx create-react-app maggie-app
cd maggie-app
npm start
```

###  1. 安装Ant Design

可以直接新建一个项目

```shell
npx create-react-app antd-demo
```

也可以用npm或者yarn安装antd，然后引入项目

> 详见官方文档[https://ant.design/docs/react/use-with-create-react-app-cn](https://ant.design/docs/react/use-with-create-react-app-cn)

### 2. 结合react-router-dom， react-redux 简单全家桶搭建

下载需要的包文件

```shell
npm install react-router-dom react-dom redux-thunk redux react-redux -D
```

p首页index.js的东西， createStore 创建1个redux 放入需要维护的全局数据counter，redux-thunk是让react支持异步操作, react-redux里面的Provider是需要包含所有节点，实现数据的共享，让需要用到数据的路由通过 import {connect} from 'react-redux' 里面的connect来获取Provider共享的数据