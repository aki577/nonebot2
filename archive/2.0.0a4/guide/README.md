# 概览

:::tip 提示
如果在阅读本文档时遇到难以理解的词汇，请随时查阅 [术语表](../glossary.md) 或使用 [Google 搜索](https://www.google.com/)。
:::

:::tip 提示
初次使用时可能会觉得这里的概览过于枯燥，可以先简单略读之后直接前往 [安装](./installation.md) 查看安装方法，并进行后续的基础使用教程。
:::

NoneBot2 是一个可扩展的 Python 异步机器人框架，它会对机器人收到的消息进行解析和处理，并以插件化的形式，分发给消息所对应的命令处理器和自然语言处理器，来完成具体的功能。

除了起到解析消息的作用，NoneBot 还为插件提供了大量实用的预设操作和权限控制机制，尤其对于命令处理器，它更是提供了完善且易用的会话机制和内部调用机制，以分别适应命令的连续交互和插件内部功能复用等需求。

目前 NoneBot2 在 [FastAPI](https://fastapi.tiangolo.com/) 的基础上封装了与 [CQHTTP(OneBot) 协议](http://cqhttp.cc/)插件的网络交互。

得益于 Python 的 [asyncio](https://docs.python.org/3/library/asyncio.html) 机制，NoneBot 处理消息的吞吐量有了很大的保障，再配合 WebSocket 通信方式（也是最建议的通信方式），NoneBot 的性能可以达到 HTTP 通信方式的两倍以上，相较于传统同步 I/O 的 HTTP 通信，更是有质的飞跃。

需要注意的是，NoneBot 仅支持 Python 3.7+ 及 CQHTTP(OneBot) 插件 v11+。

## 它如何工作？

<!-- TODO: how to work -->

~~未填坑~~

## 特色

- 提供直观的测试前端
- 提供使用简易的脚手架
- 基于异步 I/O
- 同时支持 HTTP 和反向 WebSocket 通信方式
- 支持多个机器人账号负载均衡
- 提供直观的交互式会话接口
- 提供可自定义的权限控制机制
- 多种方式渲染要发送的消息内容，使对话足够自然