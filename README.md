# flutter_widgets_doc

### Widgets目录

* [基础组件](https://www.baidu.com) - 在构建您的第一个Flutter应用程序之前，您绝对需要了解这些widget
	* [Container]() - 一个拥有绘制、定位、调整大小的 widget。
	* [Row]() - 在水平方向上排列子widget的列表。
	* [Column]() - 在垂直方向上排列子widget的列表。
	* [Image]() - 一个显示图片的widget
	* [Text]() - 单一格式的文本
	* [Icon]() - A Material Design icon
	* [RaisedButton]() - Material Design中的button， 一个凸起的材质矩形按钮
	* [Scaffold]() - Material Design布局结构的基本实现。此类提供了用于显示drawer、snackbar和底部sheet的API。
	* [Appbar]() - 一个Material Design应用程序栏，由工具栏和其他可能的widget（如TabBar和FlexibleSpaceBar）组成。
	* [FlutterLogo]() - Flutter logo, 以widget形式. 这个widget遵从IconTheme。
	* [Placeholder]() - 一个绘制了一个盒子的的widget，代表日后有widget将会被添加到该盒子中

<br />

* [Material Components Widgets](https://www.baidu.com) - 实现了Material Design 指南的视觉、效果、motion-rich的widget。
	* [App结构和导航]() - Scaffold/Appbar/BottomNavigationBar/TabBar/TabBarView/MaterialApp/WidgetsApp/Drawer
	* [按钮]() - RaisedButton/FloatingActionButton/FlatButton/IconButton/PopupMenuButton/ButtonBar
	* [输入框和选择框]() - TextField/Checkbox/Radio/Switch/Slider/Date & Time Pickers
	* [对话框、Alert、Panel]() - SimpleDialog/AlertDialog/BottomSheet/ExpansionPanel/SnackBar
	* [信息展示]() - Image/Icon/Chip/Tooltip/DataTable/Card/LinearProgressIndicator
	* [布局]() - ListTile/Stepper/Divider
	
<br />

* [Cupertino (iOS风格) Widgets](https://www.baidu.com) - 排列其它widget的columns、rows、grids和其它的layouts。
    * [CupertinoActivityIndicator]() - 一个iOS风格的loading指示器。显示一个圆形的转圈菊花
    * [CupertinoAlertDialog]() - iOS风格的alert dialog
    * [CupertinoButton]() - iOS风格的button.
    * [CupertinoDialog]() - iOS风格的对话框
    * [CupertinoDialogAction]() - 通常用于CupertinoAlertDialog的一个button
    * [CupertinoSlider]() - 从一个范围中选一个值
    * [CupertinoSwitch]() - iOS风格的开关. 用于单一状态的开/关
    * [CupertinoPageTransition]() - 提供iOS风格的页面过度动画
    * [CupertinoFullscreenDialogTransition]() - 一个iOS风格的过渡，用于调用全屏对话框。
    * [CupertinoNavigationBar]() - iOS风格的导航栏. 通常和CupertinoPageScaffold一起使用
    * [CupertinoTabBar]() - iOS风格的底部选项卡。 通常和CupertinoTabScaffold一起使用。
    * [CupertinoPageScaffold]() - 一个iOS风格的页面的基本布局结构。包含内容和导航栏
    * [CupertinoTabScaffold]() - 标签式iOS应用程序的结构。将选项卡栏放在内容选项卡之上
    * [CupertinoTabView]() - 支持选项卡间并行导航项卡的根内容。通常与CupertinoTabScaffolde一起使用


<br />

* [布局 Widget](https://www.baidu.com) - 排列其它widget的columns、rows、grids和其它的layouts。
	* [拥有单个子元素的布局widget]() - Container/Padding/Center/Align/FittedBox/AspectRatio/ConstrainedBox/Baseline/FractionallySizedBox/IntrinsicHeight/IntrinsicWidth/LimitedBox/Offstage/OverflowBox/SizedBox/SizedOverflowBox/Transform/CustomSingleChildLayout
	* [拥有多个子元素的布局widget]() - Row/Column/Stack/IndexedStack/Flow/Wrap/ListBody/ListView/CustomMultiChildLayout
	* [Layout helpers]() - LayoutBuilder


<br />

* [文本 Widget](https://www.baidu.com) - 文本显示和样式
	* [Text]() - 单一格式的文本
	* [RichText]() - 一个富文本Text，可以显示多种样式的text。
	* [DefaultTextStyle]() - 文字样式，用于指定Text widget的文字样式

<br />

* [Assets、Images、Icon](https://www.baidu.com) - 管理assets, 显示图片和Icon。
	* [Image]() - 一个显示图片的widget
	* [Icon]() - A Material Design icon
	* [RawImage]() - 一个直接显示dart:ui.Image的widget
	* [AssetBundle]() - 包含应用程序可以使用的资源，如图像和字符串。对这些资源的访问是异步，所以他们可以来自网络（例如，从NetworkAssetBundle）或从本地文件系统，这并不会挂起用户界面


<br />

* [表单 Widgets](https://www.baidu.com) - Material Components 和 Cupertino中获取用户输入的widget。
	* [Form]() - 一个可选的、用于给多个TextField分组的widget
	* [FormField]() - 一个单独的表单字段。此widget维护表单字段的当前状态，以便在UI中直观地反映更新和验证错误。
	* [RawKeyboardListener]() - 每当用户按下或释放键盘上的键时调用回调的widget。


<br />

* [动画&Motion Widget](https://www.baidu.com) - 在您的应用中使用动画。查看Flutter中的动画总览
	* [AnimatedContainer]() - 在一段时间内逐渐改变其值的容器。
	* [AnimatedCrossFade]() - 一个widget，在两个孩子之间交叉淡入，并同时调整他们的尺寸
	* [Hero]() - 将其子项标记为hero动画候选的widget
	* [AnimatedBuilder]() - 用于构建动画的通用小部件。AnimatedBuilder在有多个widget希望有一个动画作为一个较大的建造函数部分时会非常有用。要使用AnimatedBuilder，只需构建widget并将其传给builder函数即可。
	* [DecoratedBoxTransition]() - DecoratedBox的动画版本，可以给它的Decoration不同属性使用动画
	* [FadeTransition]() - 对透明度使用动画的widget
	* [PositionedTransition]() - Positioned的动画版本，它需要一个特定的动画来将孩子的位置从动画的生命周期的起始位置移到结束位置。
	* [RotationTransition]() - 对widget使用旋转动画
	* [ScaleTransition]() - 对widget使用缩放动画
	* [SizeTransition]() - Animates its own size and clips and aligns the child.
	* [SlideTransition]() - 对相对于其正常位置的某个位置之间使用动画
	* [AnimatedDefaultTextStyle]() - 在文本样式切换时使用动画
	* [AnimatedListState]() - 动画列表的state
	* [AnimatedModalBarrier]() - 一个阻止用户与widget交互的widget
	* [AnimatedOpacity]() - Opacity的动画版本，在给定的透明度变化时，自动地在给定的一段时间内改变孩子的Opacity
	* [AnimatedPhysicalModel]() - PhysicalModel的动画版本
	* [AnimatedPositioned]() - 动画版本的Positioned，每当给定位置的变化，自动在给定的时间内转换孩子的位置。
	* [AnimatedSize]() - 动画widget，当给定的孩子的大小变化时，它自动地在给定时间内转换它的大小。
	* [AnimatedWidget]() - 当给定的Listenable改变值时，会重新构建该widget
	* [AnimatedWidgetBaseState]() - 具有隐式动画的widget的基类


<br />

* [交互模型Widget](https://www.baidu.com) - 响应触摸事件并将用户路由到不同的页面视图（View）。
	* [LongPressDraggable]() - 可以使其子widget在长按时可拖动
	* [GestureDetector]() - 一个检测手势的widget
	* [DragTarget]() - 一个拖动的目标widget，在完成拖动时它可以接收数据
	* [Dismissible]() - 可以在拖动时隐藏的widget
	* [IgnorePointer]() - 在hit test中不可见的widget。当ignoring为true时，此widget及其子树不响应事件。但它在布局过程中仍然消耗空间，并像往常一样绘制它的孩子。它是无法捕获事件对象、因为它在RenderBox.hitTest中返回false
	* [AbsorbPointer]() - 在hit test期间吸收(拦截)事件。当absorbing为true时，此小部件阻止其子树通过终止命中测试来接收指针事件。它在布局过程中仍然消耗空间，并像往常一样绘制它的孩子。它只是防止其孩子成为事件命中目标，因为它从RenderBox.hitTest返回true。
	* [Navigator]() - 导航器，可以在多个页面(路由)栈之间跳转。
	* [Scrollable]() - 实现了可滚动widget的交互模型，但不包含UI显示相关的逻辑


<br />

* [样式 Widget](https://www.baidu.com) - 管理应用的主题，使应用能够响应式的适应屏幕尺寸或添加填充。
	* [Padding]() - 一个widget, 会给其子widget添加指定的填充
	* [Theme]() - 将主题应用于子widget。主题描述了应用选择的颜色和字体。
	* [MediaQuery]() - 建立一个子树，在树中媒体查询解析不同的给定数据


<br />

* [绘制和视觉效果Widget](https://www.baidu.com) - Widget将视觉效果应用到其子组件，而不改变它们的布局、大小和位置。
	* [Opacity]() - 使其子widget透明的widget。
	* [Transform]() - 在绘制子widget之前应用转换的widget
	* [DecoratedBox]() - 在孩子绘制之前或之后绘制装饰的widget。
	* [FractionalTranslation]() - 绘制盒子之前给其添加一个偏移转换
	* [RotatedBox]() - 可以延顺时针以90度的倍数旋转其子widget
	* [ClipOval]() - 用椭圆剪辑其孩子的widget
	* [ClipPath]() - 用path剪辑其孩子的widget
	* [ClipRect]() - 用矩形剪辑其孩子的widget
	* [CustomPaint]() - 提供一个画布的widget，在绘制阶段可以在画布上绘制自定义图形
	* [BackdropFilter]() - 一个widget，它将过滤器应用到现有的绘图内容，然后绘制孩子。这种效果是比较昂贵的，尤其是如果过滤器是non-local，如blur。

<br />

* [异步 Widgets](https://www.baidu.com) - Flutter应用的异步模型
	* [FutureBuilder]() - 基于与Future交互的最新快照来构建自身的widget
	* [StreamBuilder]() - 基于与流交互的最新快照构建自身的widget

<br />

* [可滚动的Widget](https://www.baidu.com) - 滚动一个拥有多个子组件的父组件
	* [ListView]() - 一个可滚动的列表
	* [NestedScrollView]() - 一个可以嵌套其它可滚动widget的widget
	* [GridView]() - 一个可滚动的二维空间数组
	* [SingleChildScrollView]() - 有一个子widget的可滚动的widget，子内容超过父容器时可以滚动。
	* [Scrollable]() - 实现了可滚动widget的交互模型，但不包含UI显示相关的逻辑
	* [Scrollbar]() - 一个Material Design 滚动条，表示当前滚动到了什么位置
	* [CustomScrollView]() - 一个使用slivers创建自定义的滚动效果的ScrollView
	* [NotificationListener]() - 一个用来监听树上冒泡通知的widget
	* [ScrollConfiguration]() - 控制可滚动组件在子树中的表现行为
	* [RefreshIndicator]() - Material Design下拉刷新指示器，包装一个可滚动widget


<br />

* [辅助功能 Widget](https://www.baidu.com) - 给你的App添加辅助功能(这是一个正在进行的工作)
	* [Semantics]() - 一个widget，用以描述widget树的具体语义。使用辅助工具、搜索引擎和其他语义分析软件来确定应用程序的含义。
	* [MergeSemantics]() - 合并其后代语义的widget。
	* [ExcludeSemantics]() - 删除其后代所有语义的widget



