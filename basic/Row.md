## 构造函数
```
Row({
    Key key,
    MainAxisAlignment mainAxisAlignment = MainAxisAlignment.start,
    MainAxisSize mainAxisSize = MainAxisSize.max,
    CrossAxisAlignment crossAxisAlignment = CrossAxisAlignment.center, 
    TextDirection textDirection, 
    VerticalDirection verticalDirection = VerticalDirection.down, 
    TextBaseline textBaseline, 
    List<Widget> children = const <Widget>[],
  })
```

## 参数解释
>* MainAxisAlignment：主轴方向上的对齐方式，会对child的位置起作用，默认是start。

    * center:将children放在主轴的中心
    * end：将children放在主轴的末尾
    * spaceAround：将主轴方向上的空白区域均分，是children之间的空白区域相等，但是首尾child的空白区域为1/2
    * spaceBetween：将主轴方向上的空白区域均分，但是首尾child都靠近首尾，没有间隙
    * spaceEvenly: 将主轴方向上的空白区域均分，包括首尾child
    * start: 将child放在主轴起点

>* MainAxisSize：在主轴方向占有空间的值，默认是max。

    * max: 根据传入的布局约束条件，最大化主轴方向的可用空间
    * min: 最小化主轴方向可用空间

>* CrossAxisAlignment：children在交叉轴方向的对齐方式，与MainAxisAlignment略有不同。

    * baseline: 在交叉轴方向，是children的baseline对齐，设置该值必须要设置textBaseline属性
    * center：交叉轴居中展示
    * end：在交叉轴末尾展示
    * start：起点处展示
    * stretch：填满交叉轴方向

>* VerticalDirection：定义了children摆放顺序，默认是down。

    * down:从top到bottom进行布局
    * up:从bottom到top布局
    * top对应Row以及Column的话，就是左边和顶部，bottom的话，则是右边和底部。

>* TextBaseline：使用的TextBaseline的方式，有两种

    * alphabetic：对齐字符底部的水平线
    * ideographic：对齐表意字符的水平线。


