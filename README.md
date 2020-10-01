<div align="center">
   <img width="160" src="http://img.mamoe.net/2020/02/16/a759783b42f72.png" alt="logo"></br>

   <img width="95" src="http://img.mamoe.net/2020/02/16/c4aece361224d.png" alt="title">

----

[![Gitter](https://badges.gitter.im/mamoe/mirai.svg)](https://gitter.im/mamoe/mirai?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Actions Status](https://github.com/mamoe/mirai-api-http/workflows/Gradle%20CI/badge.svg)](https://github.com/mamoe/mirai-api-http/actions)

Mirai 是一个在全平台下运行，提供 QQ Android 和 TIM PC 协议支持的高效率机器人框架

这个项目的名字来源于
     <p><a href = "http://www.kyotoanimation.co.jp/">京都动画</a>作品<a href = "https://zh.moegirl.org/zh-hans/%E5%A2%83%E7%95%8C%E7%9A%84%E5%BD%BC%E6%96%B9">《境界的彼方》</a>的<a href = "https://zh.moegirl.org/zh-hans/%E6%A0%97%E5%B1%B1%E6%9C%AA%E6%9D%A5">栗山未来(Kuriyama <b>Mirai</b>)</a></p>
     <p><a href = "https://www.crypton.co.jp/">CRYPTON</a>以<a href = "https://www.crypton.co.jp/miku_eng">初音未来</a>为代表的创作与活动<a href = "https://magicalmirai.com/2019/index_en.html">(Magical <b>Mirai</b>)</a></p>
图标以及形象由画师<a href = "">DazeCake</a>绘制
</div>

# mirai-api-http
Mirai WebSocket API (console) plugin

<b>Mirai-WebSocket-Api 插件 提供WebSocket API供所有语言使用mirai</b>



## 开始使用
0. 请首先运行[Mirai-console](https://github.com/mamoe/mirai-console)相关客户端生成plugins文件夹
1. 将`mirai-websocket-api`生成的`jar包文件`放入`plugins`文件夹中
2. 编辑`config/MiraiWSApi/setting.yml`配置文件 (没有则自行创建)
3. 再次启动[Mirai-console](https://github.com/mamoe/mirai-console)相关客户端
4. 记录日志中出现的`authKey`


#### setting.yml模板

```yaml
## 该配置为全局配置，对所有Session有效

# 可选，默认值为0.0.0.0
host: '0.0.0.0'

# 可选，默认值为7247
port: 7247

# 可选, 鉴权系统使用的用户名
user: root

# 必须, 默认密码为 ROOT, 必须修改
passwd: 1234567890  

```
有关配置的详细信息请参考[文档-其他](#文档).

## 更新日志
[点我查看](CHANGELOG.md)

## 文档

* **[API文档参考](docs/API.md)**
  * [状态码](docs/API.md#状态码)
  * [获取插件信息](docs/API.md#获取插件信息)
  * [认证与会话](docs/API.md#认证与会话)
    * [开始认证](docs/API.md#开始认证)
    * [校验Session](docs/API.md#校验session)
    * [释放Session](docs/API.md#释放session)
  * [消息发送与撤回](docs/API.md#消息发送与撤回)
    * [发送好友消息](docs/API.md#发送好友消息)
    * [发送临时会话消息](docs/API.md#发送临时会话消息)
    * [发送群消息](docs/API.md#发送群消息)
    * [撤回消息](docs/API.md#撤回消息)
    * [发送图片消息（通过URL）](docs/API.md#发送图片消息通过url)
  * [多媒体内容上传](docs/API.md#多媒体内容上传)
    * [图片文件上传](docs/API.md#图片文件上传)
    * [语音文件上传](docs/API.md#语音文件上传)
  * [接收消息与事件](docs/API.md#接收消息与事件)
    * [获取Bot收到的消息和事件](docs/API.md#获取bot收到的消息和事件)
    * [通过messageId获取一条被缓存的消息](docs/API.md#通过messageid获取一条被缓存的消息)
    * [查看缓存的消息总数](docs/API.md#查看缓存的消息总数)
    * [通过WebSocket](docs/API.md#通过websocket)
  * [好友与群(成员)列表](docs/API.md#好友与群成员列表)
    * [获取好友列表](docs/API.md#获取好友列表)
    * [获取群列表](docs/API.md#获取群列表)
    * [获取群成员列表](docs/API.md#获取群成员列表)
  * [群管理](docs/API.md#群管理)
    * [禁言群成员](docs/API.md#禁言群成员)
    * [解除群成员禁言](docs/API.md#解除群成员禁言)
    * [移除群成员](docs/API.md#移除群成员)
    * [退出群聊](docs/API.md#退出群聊)
    * [全体禁言](docs/API.md#全体禁言)
    * [解除全体禁言](docs/API.md#解除全体禁言)
    * [获取群设置](docs/API.md#获取群设置)
    * [修改群设置](docs/API.md#修改群设置)
    * [获取群员资料](docs/API.md#获取群员资料)
    * [修改群员资料](docs/API.md#修改群员资料)
  * [Session配置](docs/API.md#session配置)
    * [获取指定Session的配置](docs/API.md#获取指定session的配置)
    * [修改指定Session的配置](docs/API.md#修改指定session的配置)
  * [插件与Console](docs/API.md#插件与console)
    * [简介](docs/API.md#简介)
    * [注册指令](docs/API.md#注册指令)
    * [发送指令](docs/API.md#发送指令)
    * [监听指令](docs/API.md#监听指令)
    * [获取Mangers](docs/API.md#获取mangers)
* **[事件类型参考](docs/EventType.md)**
  * [Bot自身事件](docs/EventType.md#bot自身事件)
  * [消息撤回](docs/EventType.md#消息撤回)
  * [群变化事件](docs/EventType.md#群变化事件)
  * [申请事件](docs/EventType.md#申请事件)
* **[消息类型参考](docs/MessageType.md)**
* **其他**
  * [心跳](docs/Heartbeat.md)
  * [事件上报](docs/Report.md)