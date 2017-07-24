# ticTacToe（MVVM）

> Example of Model View ViewModel with Databinding .

咋一看，MVVM与MVP类似，因为他们都是抽象View的状态和展示，如果MVP模式意味着Presenter直接在View中显示该视图，则在MVVM中，
ViewModel会暴露View可以绑定到的事件流。 像这样，ViewModel不需要持有对View的引用，就像Presenter一样。 
这也意味着MVP模式所需的所有接口现在已被删除(直接DataBinding替换掉了接口).
MVVM结合了MVP提供的关注分离的优势，同时利用数据绑定的优势。结果是一个模式，其中模型驱动尽可能多的操作，使视图中的逻辑最小化。

> MVVM 模式将 Presenter 改名为 ViewModel，基本上与 MVP 模式一致。
唯一的区别在于，它采用双向绑定（data-binding）：View的变动，自动反映在ViewModel中，反之亦然，Angularh和Ember都采用这种模式

* DataModel：抽象数据源，ViewModel与DataModel一起使用来获取和保存数据源
* View：与用户交互，并且通知Viewmodel进行通信更新数据
* ViewModel：暴露与View相关的数据流

### 回到Android

在Android中应用MVVP：

Model: 表示应用业务逻辑的数据模型，本应用是指Board,Cell,Player

View：显示应用的外观，本应用里面是指Activity，Fragment，View

ViewModel：将两个对象链接在一起，处理视图逻辑，本应用是指TicTacToeViewModel




