---
icon: arrow-down-right
---

# 为什么禁用 WebRTC 不能避免被识别

许多反检测浏览器会禁用 <mark style="color:purple;">WebRTC</mark>，以防止真实 IP 地址泄漏。然而，禁用 WebRTC 本身也可能成为反欺诈系统的识别信号。大多数普通用户的 WebRTC 都可以正常工作，因此它完全不可用并不符合常见行为。

如果配置文件没有原生 UDP 支持，执行 WebRTC 检查的网站可能会收到空的 ICE 候选项列表。真实地址不会暴露，但网站能发现浏览器行为与标准配置不同，并可能提高风险评分。

正确的处理方式是保持 WebRTC 启用，并通过代理转发其 UDP 流量。客户端程序和代理都必须支持 `UDP ASSOCIATE`。

所有 ProxyShard 产品都支持通过 SOCKS5 连接传输 UDP。可用程序请参阅[启用 WebRTC 的软件方案](webrtc-software-solutions.md)。
