
#jquery.hiSlider.js 1.0
##js焦点图插件，支持移动端


在线演示：[http://www.html888.com/hiSlider](http://www.html888.com/hiSlider/)

Written by: hishion

##使用步骤

###引入资源文件


```html
<!-- jQuery library -->
<script src="js/jquery.1.9.1.js"></script>
<!-- hiSlider Javascript file -->
<script src="js/jquery.hiSlider.js"></script>
<!-- hiSlider CSS file -->
<link href="css/jquery.hiSlider.css" rel="stylesheet" />
```

###Step 2: 编写html

```html
<ul class="hiSlider">
    <li data-title="11111" class="hiSlider-item"><img src="images/1.jpg" alt="11111"></li>
    <li data-title="22222" class="hiSlider-item"><img src="images/2.jpg" alt="22222"></li>
    <li data-title="33333" class="hiSlider-item"><img src="images/3.jpg" alt="33333"></li>
    <li data-title="44444" class="hiSlider-item"><img src="images/4.jpg" alt="44444"></li>
    <li data-title="55555" class="hiSlider-item"><img src="images/5.jpg" alt="55555"></li>
</ul>
```

###Step 3: 调用 hiSlider 

```javascript
$(document).ready(function(){
  $('.hiSlider').hiSlider();
});
```

##配置项

以下参数全部为默认值
```
$('.hiSlider').hiSlider({
    //开始索引 0开始
    startSlide: 0,
    //子元素选择器
    item: '.hiSlider-item',
    //是否全屏
    isFullScreen: false,
    //是否自适应
    isFlexible: false,
    //是否支持触摸 html5 transform:
    isSupportTouch: '__proto__' in {},
    //是否显示分页按钮
    isShowPage: true,
    //是否显示标题栏
    isShowTitle: true,
    //标题文本存放的属性 或者回调函数(需要返回值)
    titleAttr: 'data-title',
    //是否显示左右控制按钮
    isShowControls: true,
    //是否自动播放
    isAuto: true,
    //自动播放间隔时间
    intervalTime: 5000,
    //特效时间 
    affectTime: 300,
    //特效类型 string : fade || move
    mode: 'move',
    //方向 string: left || top
    direction: 'left',
    //开始滑动回调
    onSwipeStart: $.noop,
    //滑动中回调
    onSwipeMove: $.noop,
    //正常滑动的最小值
    minSwipeLength: 30,
    //滑动取消回调 和 minSwipeLength值有关
    onSwipeCancel: $.noop,
    //触摸结束回调 (正常触摸)
    onSwipeEnd: $.noop,
    //向左滑动回调
    onSwipeLeft: $.noop,
    //向右滑动回调
    onSwipeRight: $.noop,
    //向上滑动回调
    onSwipeTop: $.noop,
    //向下滑动回调
    onSwipeBottom: $.noop,
    //初始化后回调
    onInited:  $.noop,
    //运动前回调
    onMoveBefore: $.noop,
    //运动后回调
    onMoveAfter: $.noop,
    //分页选中回调
    onSelected: $.noop
}); 
```

