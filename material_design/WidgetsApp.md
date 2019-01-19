未经过改装的MaterialApp
可以说MaterialApp基于WidgetsApp

## 与MaterialApp相比18个相同字段:

|字段|类型|
|-----|-----|
|navigatorKey（导航键）|GlobalKey<NavigatorState>|
|home（主页）|Widget|
|routes（路由）|Map<String, WidgetBuilder>|
|initialRoute（初始路由）|String|
|onGenerateRoute（生成路由）|RouteFactory|
|onUnknownRoute（未知路由）|RouteFactory|
|navigatorObservers（导航观察器）|List<NavigatorObserver>|
|builder（建造者）|TransitionBuilder|
|title（标题）|String|
|onGenerateTitle（生成标题）|GenerateAppTitle|
|color（颜色）|Color|
|theme（主题）|ThemeData|
|locale(地点)|Locale|
|localizationsDelegates（本地化委托）|Iterable<LocalizationsDelegate<dynamic>>|
|localeResolutionCallback（区域分辨回调）|LocaleResolutionCallback|
|supportedLocales（支持区域）|Iterable<Locale>|
|debugShowMaterialGrid（调试显示材质网格）|bool|
|showPerformanceOverlay（显示性能叠加）|bool|
|checkerboardRasterCacheImages（棋盘格光栅缓存图像）|bool|
|checkerboardOffscreenLayers（棋盘格层）|bool|
|showSemanticsDebugger（显示语义调试器）|bool|
|debugShowCheckedModeBanner（调试显示检查模式横幅）|bool|

## 介绍WidgetsApp特有的字段


>* textStyle:为应用中的文本使用的默认样式

```
//该段代码源自flutter/material/app.dart
//因为MaterialApp都是使用Theme里面的主题色，并且一般部件使用的是MaterialApp部件，所以该textStyle为报错文字的颜色
const TextStyle _errorTextStyle= const TextStyle(
  color: const Color(0xD0FF0000),
  fontFamily: 'monospace',
  fontSize: 48.0,
  fontWeight: FontWeight.w900,
  decoration: TextDecoration.underline,
  decorationColor: const Color(0xFFFFFF00),
  decorationStyle: TextDecorationStyle.double,
  debugLabel: 'fallback style; consider putting your text in a Material',
);
new WidgetsApp(
      color: Colors.grey,
      textStyle: _myTextStyle ,
    );
```

>* debugShowWidgetInspector:当为true时，打开检查覆盖，该字段只能在检查模式下可用

>* inspectorSelectButtonBuilder:构建一个视图与视图切换的小部件，可以通过该小部件或按钮切换到检查模式（debugShowWidgetInspector==true时才有效，点击该按钮之后再点击你要检查的视图）

```
new WidgetsApp(
      debugShowWidgetInspector: true,
      inspectorSelectButtonBuilder: (BuildContext context, VoidCallback onPressed) {
          return new FloatingActionButton(
            child: const Icon(Icons.search),
            onPressed: onPressed,
            mini: true,
          );
        },
    );
```

其他字段请参考:https://www.yuque.com/newtab/flutter-widgets/vx3gp1

摘自:https://www.jianshu.com/p/57c7d66c7688
