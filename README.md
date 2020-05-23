# Redux就是这么简单--Redux初体验

## 一、前言

​		在一个业务复杂的React项目中，很多组件都保持着自己的状态，模块间和各个组件之间避免不了通信，由于React单向数据流的关系，传递一个状态可能要跨好几个文件，这点为开发带来了极大的不便。

​		虽然用发布订阅模式也可以实现组件之间状态的传递，但是对于状态的修改，也只能传递一些回调函数，并不是那么的方便，于是便有了这次的主角-Redux。

## 二、官方文档

​		见[Redux官方文档](https://www.redux.org.cn/)

​		官方文档是学习一项技术最好的参考，如果有能力阅读文档（特指英文文档），肯定要从文档入手了解这项技术。

## 三、介绍

### 核心概念

​		应用中所有的 *state* 都以一个对象树的形式储存在一个单一的 *store* 中。 惟一改变 *state* 的办法是触发 *action*，一个描述发生什么的对象。 为了描述 *action* 如何改变 *state* 树，你需要编写 *reducers*（(previoutState,action)=>newState）。

### 三大原则

#### 单一数据源

​				整个应用的*state*被储存在一棵*object tree*中，并且这个*object tree*只存在于唯一一个store中。

#### **State**是只读的

​				唯一改变*state*的方法就是触发*action*，*action*是一个用于描述已发生事件的普通对象。

#### 使用纯函数来执行就改

​				为了描述*action*如何改变*state tree*，你需要编写*reducers*。*Reducer*只是一些纯函数，接收先前的*action*和*state*。	

## 四、代码编写示例

​			简单的入门示例：

​			创建demo，`create-react-app redux-demo`

![image-20200523132219955](.\assets\image-20200523132219955.png)

​			安装需要用到的包

```shell
cd redux-demo
npm install --save redux react-redux
```

