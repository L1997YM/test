# REST API设计规范
| 版本 | 日期 | 描述 | 作者 |
| - | - | - | - |
| v1.1 | 2019.4.24 | API设计规范 | LLP |

REST是Representational State Transfer（表现层状态转移）的缩写，是用来描述创建HTTP API的标准方法的。HTTP中有8种不同的方法，包括GET、POST、PUT、DELETE、OPTIONS、HEAD、TRACE、CONNECT，常用的是GET、POST、PUT和DELETE方法。
## URI
URI = scheme "://" authority "/" path [ "?" query ][ "#" fragment ]
* scheme: 低层协议
* host: 服务器的IP地址或域名
* port: 端口
* path: 访问资源的路径
* query: 参数
* fragment: 锚点，资源id
## 状态码
* 200 – OK
* 201 – Created
* 202 – Accepted
* 400 –请求出错
* 401 – 未授权
* 404 – 找不到
* 405 – 不允许此方法
* 409 – 冲突
## 本项目
本项目使用的微信开发者工具提供的云开发模式，云开发为开发者提供了一系列的API接口，因此不需要开发者自行设计API。
[微信小程序API官方文档](https://developers.weixin.qq.com/miniprogram/dev/api/)
