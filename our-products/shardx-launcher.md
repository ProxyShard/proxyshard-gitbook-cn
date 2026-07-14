---
description: >-
  ShardX 反检测浏览器，具备独特指纹，并提供本地 API 通过 Puppeteer / Playwright 自动化配置文件
icon: fingerprint
---

# ShardX Launcher

<mark style="color:purple;">**ShardX Browser**</mark> 是我们的反检测浏览器：

## 下载与安装

<mark style="color:violet;">**包含安装步骤、代理配置和创建首个配置文件的完整指南：**</mark>

{% content-ref url="../setup-guides/shardx-browser.md" %}
[ShardX Launcher — 安装与配置指南](../setup-guides/shardx-browser.md)
{% endcontent-ref %}为每个配置文件创建独立的唯一指纹（fingerprint），为每个配置文件绑定专属代理，像不同设备上的不同用户一样同时管理数十个账号。在手动模式之上，还提供本地**自动化 API**，可通过 Puppeteer / Playwright 机器人创建、启动和操控配置文件。

#### ShardX 的功能：

* 为 <mark style="color:purple;">Windows</mark>、<mark style="color:purple;">macOS</mark> 和 <mark style="color:purple;">Linux</mark> 生成独特指纹（navigator、screen、client hints、WebGL / WebGPU 等）
* 各向量独立噪音：<mark style="color:purple;">canvas、WebGL、audio、client rects、字体、传感器</mark>
* 无限数量的配置文件，按文件夹分类管理
* 为每个配置文件绑定代理（<mark style="color:purple;">SOCKS5 / HTTP / HTTPS</mark>），添加时自动测试
* 本地 **HTTP API** 实现完整自动化
* 通过 **CDP**（Chrome DevTools Protocol）控制 — 支持 Puppeteer、Playwright 及同类工具
* 配置文件之间的 cookies 导出与导入
* 独立的 **MCP 服务器**，让 AI 智能体控制配置文件

## 指纹与反检测

ShardX 为每个配置文件注入一套一致的参数：User-Agent、平台、CPU 核心数和内存大小（永远不超过真实机器），屏幕分辨率、Sec-CH-UA 等。在此基础上，各向量分别施加**噪音** — canvas、WebGL、audio、client rects、字体、传感器。每个噪音块独立开关，因此配置文件的指纹在会话内保持稳定，但与其他配置文件及您的真实设备各不相同。

{% hint style="info" %}
指纹经过独特化处理，不与硬件绑定：CPU 核心数和内存大小根据宿主机调整，不会虚报；屏幕裁剪为真实显示器尺寸。这降低了因参数不一致被识别的风险。
{% endhint %}

## 代理、QUIC 与 WebRTC

ShardX 与我们的代理配合尤为出色。**每次**启动配置文件时，在浏览器启动之前，系统会实时探测绑定代理对 UDP-relay（SOCKS5 UDP\_ASSOCIATE）的支持情况：

* 如果 UDP 可用 — 启用 <mark style="color:purple;">QUIC</mark>，WebRTC 通过代理的 UDP relay 进行通信；
* 如果 UDP 不可用 — 禁用 QUIC，WebRTC 强制切换为 **TCP-only** 模式，防止真实 IP 泄露。

启动时，设置为 `auto` 的时区、语言和地理位置字段也会通过代理实时解析。

{% hint style="success" %}
ShardX + 我们的 [**UDP 代理**](about-udp/) 组合在浏览器层面彻底消除 WebRTC 泄露：UDP 流量经过代理，不会直接暴露您的 IP。关于该问题的详细说明，请参阅 [**关于 UDP 协议**](about-udp/) 章节。
{% endhint %}

## 自动化：本地 API

应用内部在 <mark style="color:purple;">**127.0.0.1**</mark> 上启动本地 HTTP 服务器（默认端口 **40325**，可在 _Settings → Automation API_ 修改）。外部无法访问 — 仅限本机。

除 `GET /health` 外，所有请求均需要 **Bearer 令牌**（来自设置的永久 JWT）：

```
Authorization: Bearer <token>
```

设置中的 **Regenerate token** 按钮即时轮换密钥：新令牌立即生效，所有旧令牌同时失效。

典型自动化流程：

1. `GET /fingerprint/new/{platform}` — 获取唯一化指纹（不保存）。
2. 可选择调整指纹（例如启用字体噪音或修改 WebRTC 模式）。
3. `POST /profiles` — 使用该指纹创建配置文件（原样保存，不二次随机化）并绑定代理。
4. `POST /profiles/{id}/start` — 启动配置文件，获取 **CDP 端点**。
5. 在 Puppeteer / Playwright 中以 `browserWSEndpoint = cdp.web_socket_debugger_url` 连接。
6. `POST /profiles/{id}/stop` — 关闭配置文件。

{% hint style="info" %}
**临时配置文件。** `POST /profiles/temporary` 创建带 `temporary` 标志的配置文件：在通用列表和界面中隐藏，浏览器关闭后自动删除（连同数据文件夹）。适合一次性任务。
{% endhint %}

所有方法（配置文件、指纹、代理、文件夹、cookies、启动/停止）的完整参考文档，包含数据模型和示例，请查阅 [ShardX Launcher API 规范](https://docs.proxyshard.com/cn/shardx-launcher-api/binding-and-lifecycle)。

## 面向 AI 智能体的 MCP 服务器

随附独立的 **MCP 服务器**（Model Context Protocol）：允许 AI 客户端通过同一 API 控制启动器，并通过 CDP 控制配置文件的浏览器。这是一个独立的 Node 进程，不属于 HTTP API 的一部分。

可直接从启动器下载（_Settings → MCP server → Download MCP server_）。配置两个变量即可：`SHARDX_API`（API 基础 URL）和 `SHARDX_TOKEN`（Bearer 令牌）。MCP 服务器提供：

* **API 工具** — 启动器方法的轻量封装（配置文件、指纹、代理、文件夹、cookies、启动/停止）；
* **浏览器工具**，基于 CDP — 导航、JS 执行、截图、点击、文本输入、标签页管理和等待操作。

{% hint style="warning" %}
CDP（远程调试）**仅**在通过 API 启动配置文件时启用。通过界面启动不会开启调试端口 — 反检测能力不受影响。
{% endhint %}
