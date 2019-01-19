## 构造函数

```
({
    Key key,
    @required this.items,
    this.onTap,
    this.currentIndex = 0,
    BottomNavigationBarType type,
    this.fixedColor,
    this.iconSize = 24.0,
  }) 
```

## 参数解释

>* onTap: 点击事件

>* currentIndex: 当前选中的位置,不能超过items.length

>* BottomNavigationBarType: 是BottomNavigationBarItem的样式展示: fixed表示BottomNavigationBarItem的内容都是固定的,不会变化; shifting表示只有当前index被选中的时候,才展示BottomNavigationBarItem中的title字段,其他情况只显示icon

>* items: 构造函数:

```
BottomNavigationBarItem({
  @required this.icon, //图标
  @required this.title, //标题
  Widget activeIcon, //被选中的时候展示的icon,不设置就展示icon字段
  this.backgroundColor,//背景颜色
})
```


>* fixedColor:当BottomNavigationBarType为fixed的时候,被选中的那一个
BottomNavigationBarItem的颜色,如果BottomNavigationBarType为shifting,则忽略这个字段

>* iconSize:  BottomNavigationBarItem中的icons大小
