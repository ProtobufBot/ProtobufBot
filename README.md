# ProtobufBot

[![QQ群](https://img.shields.io/static/v1?label=QQ%E7%BE%A4&message=335783090&color=blue)](https://jq.qq.com/?_wv=1027&k=B7Of3GMZ)

## 可用的编程语言和对应框架（SDK）

| 语言           | 框架地址                                                     | Demo                                                         | 核心作者                                  | 备注                                                         |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| Java<br>Kotlin | [protobufbot/pbbot-spring-boot-starter](https://github.com/protobufbot/pbbot-spring-boot-starter) | [protobufbot/spring-mirai-server](https://github.com/protobufbot/spring-mirai-server) | [lz1998](https://github.com/lz1998)       | 有插件机制                                                   |
| Node.js        | [ProtobufBot/js-pbbot](https://github.com/ProtobufBot/js-pbbot) | [example](https://github.com/ProtobufBot/js-pbbot/tree/master/example) | [lz1998](https://github.com/lz1998)       |                                                              |
| Python         | [PHIKN1GHT/pypbbot](https://github.com/PHIKN1GHT/pypbbot)    | [example](https://github.com/PHIKN1GHT/pypbbot/tree/main/pypbbot_examples) | [PHIKN1GHT](https://github.com/PHIKN1GHT) | [文档](https://pypbbot.kale1d0.space/) 有插件机制 |
| Golang         | [ProtobufBot/go-pbbot](https://github.com/protobufbot/go-pbbot) | [test](https://github.com/ProtobufBot/go-pbbot/blob/master/test/bot_test.go) | [lz1998](https://github.com/lz1998)       |  
| C++         | [ProtobufBot/cpp-pbbot](https://github.com/ProtobufBot/cpp-pbbot) | [event_handler](https://github.com/ProtobufBot/cpp-pbbot/blob/main/src/event_handler/event_handler.cpp) | [lz1998](https://github.com/lz1998)       | 依赖[Drogon](https://github.com/an-tao/drogon)，需要CMake |
| Rust         | - | [rs-demo](https://github.com/ProtobufBot/rs-demo) | [lz1998](https://github.com/lz1998)  [NKDark](https://github.com/NKDark)       | 基本能用，正在开发 |
| 易语言         | [ProtobufBot/pbbot_e_sdk](https://github.com/protobufbot/pbbot_e_sdk) | 包含在框架内                                                 | GhostSn                                   | 只有常用功能                                                 |

推荐**直接看Demo**，根据demo直接修改，快速上手

#### 其他语言

编写websocket server，使用二进制数据通信。消息处理代码可以使用[onebot_idl](https://github.com/ProtobufBot/onebot_idl)自动生成。参考[Protobuf](https://developers.google.com/protocol-buffers)官网，使用protoc自动生成代码，官方支持C++ C# Dart Go Java Python，通过安装protoc插件可以支持更多语言。 

## QQ机器人的软件（相当于酷Q）

| 软件                                                         | 协议库  | 环境   | 备注                                       |
| ------------------------------------------------------------ | ------- | ------ | ------------------------------------------ |
| [GMC](https://github.com/protobufbot/go-Mirai-Client/releases)**【推荐】** | miraigo | 不需要 | 一个程序可以登陆一个号，多个号需要多开     |
| [SMC](https://github.com/protobufbot/spring-Mirai-Client/releases) | mirai   | JVM    | 一个程序可以登陆多个号，但是没上面稳定好用 |

## 注意

以上两者需要同时运行，代码写在第一个里面，第二个只需要运行

## 整体流程:

- 先运行GMC/SMC(二选一)并登陆, 然后选择任意编程语言，编写代码后运行，需要与GMC/SMC同时运行。
- GMC/SMC收到消息后会通过websocket上报给消息处理端，如果需要发送消息，消息处理端会通过websocket通知GMC/SMC发送消息。

## 推荐的使用方法
先运行GMC/SMC + Demo，不修改任何代码，运行成功后再进行修改。


![](https://github.com/ProtobufBot/ProtobufBot/blob/main/architecture.jpg?raw=true)
