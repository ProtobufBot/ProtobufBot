# ProtobufBot

## 可用的编程语言和对应框架（SDK）

1. Java/Kotlin
    - 框架: SpringBoot + pbbot-spring-boot-starter
    - Demo链接: https://github.com/protobufbot/spring-mirai-server

2. JavaScript/TypeScript
    - 框架: js-pbbot
    - Demo链接: https://github.com/ProtobufBot/js-pbbot/tree/master/example

3. 易语言
    - SDK: https://github.com/ProtobufBot/pbbot_e_sdk
    - 代码在"机器人处理程序集"

## QQ机器人的软件（相当于酷Q）
- GMC(不需要环境): https://github.com/protobufbot/go-Mirai-Client/releases
- SMC(需要jvm环境): https://github.com/protobufbot/spring-Mirai-Client/releases

## 整体流程:
- 先运行GMC/SMC(二选一)并登陆, 然后选择任意编程语言，编写代码后运行，需要与GMC/SMC同时运行。
- GMC/SMC收到消息后会通过websocket上报给消息处理端，如果需要发送消息，消息处理端会通过websocket通知GMC/SMC发送消息。

## 推荐的使用方法
先运行GMC/SMC + Demo，不修改任何代码，运行成功后再进行修改。
