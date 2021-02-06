# fed-e-task-04-05
antd+react+typescript

请完成下面几道简答题。

1.通过该项目，请简要说明 typescript 比 javascript 的优势在哪？
1、Typescript出现的原因
JavaScript 是轻量级的解释性脚本语言，可嵌入到 HTML 页面中，在浏览器端执行，但是JavaScript不适合开发大型的项目，没有面向对象的设计理念。所以出现了TypeScript来解决JavaScript的缺陷。

TypeScript 是JavaScript 的超集，即包含JavaScript 的所有元素，能运行JavaScript 的代码，并扩展了JavaScript 的语法。相比于JavaScript ，它还增加了静态类型、类、模块、接口和类型注解方面的功能，更易于大项目的开发。

2、Typescript到底有哪些优势呢？
（1）、便于开发人员做注释。

（2）、能帮助开发人员检测出错误并修改。

（3）、TypeScript工具使重构更变的容易、快捷。

（4）、TypeScript 引入了 JavaScript 中没有的“类”概念。

（5）、TypeScript 中引入了模块的概念，可以把声明、数据、函数和类封装在模块中。

（6）、类型安全功能能在编码期间检测错误，这为开发人员创建了一个更高效的编码和调试过程。


2.请简述一下支付流程
调接口支付


3.react-redux 的主要作用是什么，常用的 api 有哪些，什么作用？
每次都重新调用render和getState太low了，想更方便的实现功能我们可以使react-redux
React-Redux是在Redux的基础上，将其大量重复的代码进行了封装。
api
1. Provider
利用context对象给所有子组件提供store。不再需要在每个组件都引用store

2. connect
该方法封装了大量的逻辑，主要如下：
 1. 给使用connect方法的组件属性自动绑定了dispatch方法；this.props.dispatch
 2. 给使用connect方法的组件的setState方法自动添加了对仓库的state的订阅
 3. 给使用connect方法的组件的属性绑定仓库的state值；this.props.XXXX
    不再使用store.getState方法
 4. 给使用connect方法的组件的actions自动使用bindActionCreators方法

4.redux 中的异步如何处理？
本质是一个函数，redux默认是处理不了异步action

异步action中第1个参数叫dispatch，第2个参数是getState
在异步action中就可以写异步代码
在异步代码，还需要派发一个同步的action