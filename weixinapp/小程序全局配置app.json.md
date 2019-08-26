# app.json文件的全局主要配置。

#### 小程序根目录下的 app.json 文件用来对微信小程序进行全局配置。
***
#### pages：
##### 主要是对页面进行路由的配置与注册。每一项都对应一个页面的 路径（含文件名） 信息。文件名不需要写文件后缀，框架会自动去寻找对于位置的 .json, .js, .wxml, .wxss 四个文件进行处理。所以这四个文件必须同名。数组的第一项的路径即为微信小程序首页的路径。

```
{
  "pages": [
    "pages/indexZt/indexZt",
    "pages/index/index",
  ],
}
```
***
#### window：
##### 用于设置小程序的状态栏、导航条、标题、窗口背景色。
```
"window": {
    //设置窗口背景的颜色
    "backgroundColor": "#F6F6F6",
    //设置下拉 loading 的样式(三个loading小圆点的颜色)，仅支持 dark / light
    "backgroundTextStyle": "light",
    //可设置头部导航栏背景颜色
    "navigationBarBackgroundColor": "#000",
    //设置头部导航栏文字标题
    "navigationBarTitleText": "张婷的微信小程序",
    //设置导航栏文字标题颜色仅支持仅支持 black / white
    "navigationBarTextStyle": "black",
    //导航栏样式，仅支持以下值：default(默认导航栏)/custom（自定义导航栏，仅保留右上角胶囊按钮）
    navigationStyle："default",
    //顶部窗口的颜色，仅ios
    backgroundColorTop:"#ffffff",
    //底部窗口的颜色，仅ios
    backgroundColorBottom:'#ffffff',
    //是否开启全局下拉刷新
    "enablePullDownRefresh":true,
    //页面上拉触底事件触发时距页面底部距离，单位为 px。
    "onReachBottomDistance":50,
    //屏幕旋转设置，支持 auto / portrait / landscape
    "pageOrientation","auto"

  },
```

##### [navigationStyle](./小程序适配ios以及安卓的自定义导航栏.md)具体使用说明，以及封装自定义导航栏适配多种机型。

##### enablePullDownRefresh，onReachBottomDistance下拉刷新以及上拉触底的具体使用
