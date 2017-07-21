# ticTacToe(MVC)

> Is an example of using Model View Controller to model the UI / Model Interaction.

**（Model）、（View）（Controller)**

* 控制器（Controller）- 负责转发请求，对请求进行处理。

* 视图（View） - 界面设计人员进行图形界面设计。

* 模型（Model） - 程序员编写程序应有的功能（实现算法等等）、数据库专家进行数据管理和数据库设计(可以实现具体的功能)。

MVC之间典型的关系：

![From 维基百科](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/400px-MVC-Process.svg.png)

在MVC设计模式中， Model 响应用户请求并返回响应数据，View 负责格式化数据并把它们呈现给用户，业务逻辑和表示层分离，
同一个 Model 可以被不同的 View 重用，所以大大提高了代码的可重用性。其次，Controller 是自包含（self-contained）指高独立内聚的对象，
与 Model 和 View 保持相对独立，所以可以方便的改变应用程序的数据层和业务规则.

MVC 模式的应用程序的目的就是希望打破以往应用程序使用的大杂烩程序撰写方式，并间接诱使开发人员以更高的架构导向思维来思考应用程序的设计。

这里有一个通过 JavaScript 所实现的一个基础 MVC 模型，**请注意的是：MVC 不是一种技术，仅是一种理念**。

```
/**  Model, View, Controller */
var M = {}, V = {}, C = {};

/** Model 負責存放資料 */
M.data = "hello world";

/** View 負責將資料輸出到螢幕上 */
V.render = (M) => { alert(M.data); }

/** Controller 作為一個 M 和 V 的橋樑 */
C.handleOnload = () => { V.render(M); }

/** 在網頁讀取的時候呼叫 Controller */
window.onload = C.handleOnload;
```

在这个简短的代码中就具有一个完整的 MVC 模式。

## 回到Android

在Android中应用MVC：

Model: 主要处理数据和业务逻辑这块，本应用里面即是Board，Cell，Player

View：主要是XML文件，是Model的界面展示，并且与Controller通信

Controller：主要是Activity，Fragment，链接View和Model

> View和Controller之间互相通信，Controller和Model之间通信，View和Model之间是隔离的










