# ticTacToe(MVP)

> Is an example of using Model View Presenter

**(Model)  (View)  (Presenter)**

* Model：定义与用户交互界面所需要被显示的数据模型，一个模型包含着相关的业务逻辑。
* View：视图为呈现使用者界面的终端，用以表现来自 Model 的数据，和使用者命令路由再经过 Presenter 对事件处理后的数据。
* Presenter：包含着View的事件处理，负责检索 Model 取得数据，和将取得的数据经过格式转换与 View 进行通信。

![来自网络](http://image.beekka.com/blog/2015/bg2015020109.png)

1. 各部分之间的通信，都是双向的。
2. View 与 Model 不发生联系，都通过 Presenter 传递。
3. View 非常薄，不部署任何业务逻辑，称为"被动视图"（Passive View），即没有任何主动性，而 Presenter非常厚，所有逻辑都部署在那里。


### 回到Android

> 在Android中应用MVP：

* Model: 在好的分层架构的应用中，Model应该是数据层的唯一入口，网络请求获取数据亦或是数据库等本地序列化存储的数据
* View: 通常有Activity（Fragment，View）承载，与Presenter链接，与Model隔离，View与用户交互对应的处理逻辑，需要Presenter提供
* Presenter: 链接View和Model之间的桥梁，它从Model中获取数据，处理后返回给View,与MVC不同的是，它会在与View交互的时候，处理相应业务逻辑
所以它里面的东西非常多




