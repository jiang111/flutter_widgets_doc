## 简介
Scaffold 实现了基本的纸墨设计布局结构。在示例应用中，MyHomePage 所返回的就是一个 Scaffold。也就是说， MaterialApp 的 child 是 Scaffold Widget。 <br />

在纸墨设计中定义的单个界面上的各种布局元素，在 Scaffold 中都有支持，比如 左边栏（Drawers）、snack bars、以及 bottom sheets。


## 构造函数
```
Scaffold({
    Key key,
    this.appBar,
    this.body,
    this.floatingActionButton,
    this.floatingActionButtonLocation,
    this.floatingActionButtonAnimator,
    this.persistentFooterButtons,
    this.drawer,
    this.endDrawer,
    this.bottomNavigationBar,
    this.bottomSheet,
    this.backgroundColor,
    this.resizeToAvoidBottomPadding = true,
    this.primary = true,
  })
```

## 参数解释
>* [appBar](Appbar.md)：显示在界面顶部的一个 AppBar，也就是 Android 中的 ActionBar 、Toolbar
>* body：当前界面所显示的主要内容 Widget
>* floatingActionButton：纸墨设计中所定义的 FAB，界面的主要功能按钮
>* persistentFooterButtons：固定在下方显示的按钮，比如对话框下方的确定、取消按钮
>* drawer：侧边栏控件
>* backgroundColor： 内容的背景颜色，默认使用的是 ThemeData.scaffoldBackgroundColor 的值
>* bottomNavigationBar： 显示在页面底部的导航栏
>* resizeToAvoidBottomPadding：类似于 Android 中的 android:windowSoftInputMode=”adjustResize”，控制界面内容 body 是否重新布局来避免底部被覆盖了，比如当键盘显示的时候，重新布局避免被键盘盖住内容。默认值为 true。


显示 snackbar 或者 bottom sheet 的时候，需要使用当前的 BuildContext 参数调用 Scaffold.of 函数来获取 ScaffoldState 对象，然后使用 ScaffoldState.showSnackBar 和 ScaffoldState.showBottomSheet 函数来显示。

<br />

要特别注意 Scaffold.of 的参数 BuildContext， 如果包含该 BuildContext 的 Widget 是 Scaffold 的父 Widget，则 Scaffold.of 是无法查找到对应的 ScaffoldState 对象的，Scaffold.of 返回的是父对象中最近的 Scaffold 中的 ScaffoldState 对象。 比如，如果在 Scaffold 的 build 函数中，使用 build 的 BuildContext 参数是可以的：

```
@override
Widget build(BuildContext context) {
  return new RaisedButton(
    child: new Text('SHOW A SNACKBAR'),
    onPressed: () {
      Scaffold.of(context).showSnackBar(new SnackBar(
        content: new Text('Hello!'),
      ));
    },
  );
}
```

如果 build 函数返回一个 Scaffold 对象，则由于 Scaffold 对象是这个 Widget 的子对象，所以使用这个 build 的 BuildContext 参数是不能查找到 ScaffoldState 对象的，这个时候，通过在 Scaffold 中使用一个 Builder 来提供一个新的 BuildConext ：

```
@override
Widget build(BuildContext context) {
  return new Scaffold(
    appBar: new AppBar(
      title: new Text('Demo')
    ),
    body: new Builder(
      // Create an inner BuildContext so that the onPressed methods
      // can refer to the Scaffold with Scaffold.of().
      builder: (BuildContext context) {
        return new Center(
          child: new RaisedButton(
            child: new Text('SHOW A SNACKBAR'),
            onPressed: () {
              Scaffold.of(context).showSnackBar(new SnackBar(
                content: new Text('Hello!'),
              ));
            },
          ),
        );
      },
    ),
  );
}
```

另外还可以把 build 函数中的 Widget 分别创建，分别引入新的 BuildContext 来获取 Scaffold。

摘自:http://blog.chengyunfeng.com/?p=1042