# 软件架构文档

“挣他一个亿”是一款微信小程序，采用微信小程序特有的云开发模式，其架构如下：
* 前端：微信小程序前端框架
* 后端：依赖云开发快速构建后端服务

## 微信小程序前端框架
[微信小程序前端框架官方文档](https://developers.weixin.qq.com/miniprogram/dev/framework/MINA.html)

小程序开发框架的目标是通过尽可能简单、高效的方式让开发者可以在微信中开发具有原生 APP 体验的服务。

整个小程序框架系统分为两部分：逻辑层（App Service）和 视图层（View）。小程序提供了自己的视图层描述语言 WXML 和 WXSS，以及基于 JavaScript 的逻辑层框架，并在视图层与逻辑层间提供了数据传输和事件系统，让开发者能够专注于数据与逻辑。

### 逻辑层 App Service
小程序开发框架的逻辑层使用 JavaScript 引擎为小程序提供开发者 JavaScript 代码的运行环境以及微信小程序的特有功能。

逻辑层将数据进行处理后发送给视图层，同时接受视图层的事件反馈。

开发者写的所有代码最终将会打包成一份 JavaScript 文件，并在小程序启动的时候运行，直到小程序销毁。这一行为类似 ServiceWorker，所以逻辑层也称之为 App Service。

在 JavaScript 的基础上，微信增加了一些功能，以方便小程序的开发：
* 增加 App 和 Page 方法，进行程序注册和页面注册。
* 增加 getApp 和 getCurrentPages 方法，分别用来获取 App 实例和当前页面栈。
* 提供丰富的 API，如微信用户数据，扫一扫，支付等微信特有能力。
* 提供模块化能力，每个页面有独立的作用域。

### 视图层 View
框架的视图层由 WXML 与 WXSS 编写，由组件来进行展示。

将逻辑层的数据反应成视图，同时将视图层的事件发送给逻辑层。

WXML(WeiXin Markup language) 用于描述页面的结构。

WXS(WeiXin Script) 是小程序的一套脚本语言，结合 WXML，可以构建出页面的结构。

WXSS(WeiXin Style Sheet) 用于描述页面的样式。

组件(Component)是视图的基本组成单元。
