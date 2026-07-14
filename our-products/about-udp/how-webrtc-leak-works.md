---
description: WebRTC 的工作原理
icon: wave-square
---

# WebRTC 泄漏是如何发生的

1. 网站从浏览器或反检测浏览器发送常规 TCP 请求。
2. 反欺诈系统响应并注入 STUN 请求的脚本。
3. 浏览器通过 UDP 发出 STUN 请求，绕过真实地址的代理，因为代理或反检测浏览器可能不支持 UDP。
4. 如果TCP连接和UDP连接中的IP不同，则用户暴露为使用代理。<br>




