# 架构设计、详细设计（BCE方法）到应用程序框架映射指南
| 版本 | 日期 | 描述 | 作者 |
| - | - | - | - |
| v1.3 | 2019.5.26 | BCE | LLP |

## 逻辑架构
逻辑架构由三层模型（表示层、业务层、持久化层）构成
### 表示层
用户端使用微信小程序作为表示层，提供问卷调查子系统、寻物启事子系统。
### 业务层
服务器充当业务层的角色，在本项目中，服务器部署在云平台上。
### 持久化层
使用微信小程序开发者工具云开发模式，微信小程序的云平台提供了数据库，提供了数据的持久化服务。

## 框架目录设计
### 小程序
~~~
.
├── cloudfunctions
│   ├── login
│   │   │   ├── index.js
│   │   │   └── package.json
│   ├── submitQuestionaire
│   │   ├── about
│   │   │   ├── index.js
│   │   │   └── package.json
├── miniprogram
│   ├── images
│   │   └── ...
│   ├── pages
│   │   ├── about
│   │   │   ├── about.js
│   │   │   ├── about.json
│   │   │   ├── about.wxml
│   │   │   └── about.wxss
│   │   ├── answerQuestionaire
│   │   │   ├── answerQuestionaire.js
│   │   │   ├── answerQuestionaire.json
│   │   │   ├── answerQuestionaire.wxml
│   │   │   └── answerQuestionaire.wxss
│   │   ├── login
│   │   │   ├── login.js
│   │   │   ├── login.json
│   │   │   ├── login.wxml
│   │   │   └── login.wxss
│   │   ├── lostList
│   │   │   ├── lostList.js
│   │   │   ├── lostList.json
│   │   │   ├── lostList.wxml
│   │   │   └── lostList.wxss
│   │   ├── mine
│   │   │   ├── mine.js
│   │   │   ├── mine.json
│   │   │   ├── mine.wxml
│   │   │   └── mine.wxss
│   │   ├── modifyUserInfo
│   │   │   ├── modifyUserInfo.js
│   │   │   ├── modifyUserInfo.json
│   │   │   ├── modifyUserInfo.wxml
│   │   │   └── modifyUserInfo.wxss
│   │   ├── myQuestion
│   │   │   ├── myQuestion.js
│   │   │   ├── myQuestion.json
│   │   │   ├── myQuestion.wxml
│   │   │   └── myQuestion.wxss
│   │   ├── newLost
│   │   │   ├── newLost.js
│   │   │   ├── newLost.json
│   │   │   ├── newLost.wxml
│   │   │   └── newLost.wxss
│   │   ├── newQuestionaire
│   │   │   ├── newQuestionaire.js
│   │   │   ├── newQuestionaire.json
│   │   │   ├── newQuestionaire.wxml
│   │   │   └── newQuestionaire.wxss
│   │   ├── questionaireList
│   │   │   ├── questionaireList.js
│   │   │   ├── questionaireList.json
│   │   │   ├── questionaireList.wxml
│   │   │   └── questionaireList.wxss
│   │   └── statistics
│   │       ├── statistics.js
│   │       ├── statistics.json
│   │       ├── statistics.wxml
│   │       └── statistics.wxss
│   ├── style
│   │   └── guide.wxss
│   ├── utils
│   │   └── util.js
│   ├── app.js
│   ├── app.json
│   ├── app.wxss
│   └── sitemap.json
└── project.config.json
```
~~~
## EBC
* Entity:代表系统数据，本项目中主要是指数据库中的记录，例如用户信息记录、问卷记录、失物招领记录。
* Boundary:表示参与者与系统之间进行的交互和信息交流，本项目中主要是界面，如创建问卷界面、填写问卷界面、问卷列表界面。
* Controller:一个用例具有的事件流的控制行为，在 Boundary 和 Entity 中衔接的媒介，接受来自Boundary的命令并处理执行。
* EBC是框架目录设计与逻辑架构的一种具体方法。
