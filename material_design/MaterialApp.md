## 构造函数
```
MaterialApp({ // can't be const because the asserts use methods on Map :-(
    Key key,
    this.navigatorKey,
    this.home,
    this.routes = const <String, WidgetBuilder>{},
    this.initialRoute,
    this.onGenerateRoute,
    this.onUnknownRoute,
    this.navigatorObservers = const <NavigatorObserver>[],
    this.builder,
    this.title = '',
    this.onGenerateTitle,
    this.color,
    this.theme,
    this.locale,
    this.localizationsDelegates,
    this.localeResolutionCallback,
    this.supportedLocales = const <Locale>[Locale('en', 'US')],
    this.debugShowMaterialGrid = false,
    this.showPerformanceOverlay = false,
    this.checkerboardRasterCacheImages = false,
    this.checkerboardOffscreenLayers = false,
    this.showSemanticsDebugger = false,
    this.debugShowCheckedModeBanner = true,
  })
```

## 参数解释

>* home:进入程序后显示的第一个页面,传入的是一个Widget，但实际上这个Widget需要包裹一个Scaffold以显示该程序使用Material Design风格

>* routes:声明程序中有哪个通过Navigation.of(context).pushNamed跳转的路由 参数以键值对的形式传递 key:路由名字 value:对应的Widget

```
new MaterialApp(
      routes: {
       '/home':(BuildContext context) => HomePage(),
       '/home/one':(BuildContext context) => OnePage(),
       //....
      },
    );
```


>* initialRoute:初始路由，当用户进入程序时，自动打开对应的路由。 (home还是位于一级) 传入的是上面routes的key 跳转的是对应的Widget（如果该Widget有Scaffold.AppBar,并不做任何修改，左上角有返回键）

```
new MaterialApp(
      routes: {
       '/home':(BuildContext context) => HomePage(),
       '/home/one':(BuildContext context) => OnePage(),
       //....
      },
      initialRoute: '/home/one',
    );
```


>* onGenerateRoute:当通过Navigation.of(context).pushNamed跳转路由时， 在routes查找不到时，会调用该方法

>* onUnknownRoute:效果跟onGenerateRoute一样 调用顺序为onGenerateRoute ==> onUnknownRoute

>* navigatorObservers:路由观察器，当调用Navigator的相关方法时，会回调相关的操作

>* builder:当构建一个Widget前调用 一般做字体大小，方向，主题颜色等配置

>* title:该标题出现在 Android：任务管理器的程序快照之上 IOS: 程序切换管理器中

>* onGenerateTitle:跟上面的tiitle一样，但含有一个context参数 用于做本地化

>* color:该颜色为Android中程序切换中应用图标背景的颜色，当应用图标背景为透明时

>* theme:应用程序的主题，各种的定制颜色都可以设置，用于程序主题切换

>* locale:当前区域，如果为null则使用系统区域 一般用于语言切换

>* localizationsDelegates:本地化委托，用于更改Flutter Widget默认的提示语，按钮text等

>* localeResolutionCallback:当传入的是不支持的语种，可以根据这个回调，返回相近,并且支持的语种

>* supportedLocales:传入支持的语种数组

>* debugShowMaterialGrid:debug模式下是否显示材质网格，传入bool类型，使用就不写了

>* showPerformanceOverlay:当为true时应用程序顶部覆盖一层GPU和UI曲线图，可即时查看当前流畅度情况

>* checkerboardRasterCacheImages:当为true时，打开光栅缓存图像的棋盘格

>* checkerboardOffscreenLayers:当为true时，打开呈现到屏幕位图的层的棋盘格

>* showSemanticsDebugger:当为true时，打开Widget边框，类似Android开发者模式中显示布局边界

>* debugShowCheckedModeBanner:当为true时，在debug模式下显示右上角的debug字样的横幅，false即为不显示

摘自:https://juejin.im/post/5b5ed06b5188251aa30c790c