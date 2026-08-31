---
description: >-
  代理为何需要支持 UDP，以及 UDP 如何帮助降低被反欺诈系统识别的风险
icon: shield-exclamation
---

# 关于 UDP 协议

### **内容**

* [WebRTC 检测的工作原理](how-webrtc-leak-works.md)
* [如何检查 WebRTC 泄漏或功能是否正常](webrtc-leak-check-tools.md)
* [为什么禁用 WebRTC 不能避免被识别](why-blocking-webrtc-doesnt-help.md)
* [安装 Tampermonkey 和 WebRTC 调试脚本](tampermonkey-webrtc-debug.md)
* [我们的实测结果](field-test-results.md)
* [启用 WebRTC 的软件方案](webrtc-software-solutions.md)
* [常见问题](../../faq-and-support/faq/)

### **基础说明**

现代反欺诈系统会使用越来越多的方法来识别用户的真实 IP 地址，并检测用于隐藏网络流量的工具。即使您使用代理或 <mark style="color:purple;">VPN</mark>，网站仍可能通过其他信号判断流量经过了伪装。

其中一种机制与 <mark style="color:purple;">WebRTC</mark> 有关。如果代理或客户端程序不支持 UDP，或者没有正确转发这类流量，WebRTC 就可能通过 UDP 发送请求并暴露用户的真实 IP 地址。
