# 基于vue开发的移动端基础组件库

### 1.confirm组件
该组件主要是用来弹出一个对话框，来进行确认和取消处理。用于一切影响比较大的用户操作行为，如：清空购物车、清空列表、全部删除等操作。

接受的参数有：
* 1.text: 用于给用户提示信息，字符串类型默认为删除。
* 2.sureBtn: 用于提供左侧按钮信息，字符串类型默认为确认。
* 3.cancelBtn: 用于提供右侧按钮信息，字符串类型默认为取消。
* 4.showFlag: 用于组件的显示或者隐藏，布尔类型默认为false。

派发的事件：
* 1.sure: 单击左侧按钮时的回调函数，无回调参数。
* 2.cancel: 单击右侧按钮时的回调函数，无回调参数。

效果预览：

![](https://github.com/lml19960131/baseComponents/blob/master/src/test/confirm/confirm1.png)
![](https://github.com/lml19960131/baseComponents/blob/master/src/test/confirm/confirm2.png)

### 2.loading组件
该组件主要是用来提示用户信息、文件、页面、图片等正在加载。
接受的参数有：
* 1.showFLag: 用于组件的显示或隐藏，布尔类型默认为false。
* 2.text: 用于控制提示信息，默认值为正在加载。

效果预览:

1[](https://github.com/lml19960131/baseComponents/blob/master/src/test/loading/loading.png)
