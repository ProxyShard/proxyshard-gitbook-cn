---
description: >-
  Why UDP support is needed in proxies and how it helps bypass
  anti-fraud systems
icon: shield-exclamation
---

# 关于UDP协议

### **内容**

* [WebRTC检测工作原理](how-webrtc-leak-works.md)
* [如何检查WebRTC泄漏或WebRTC功能](webrtc-leak-check-tools.md)
* [为什么仅靠 TCP 代理是不够的！](why-tcp-proxy-not-enough.md)
* [启用WebRTC的软件解决方案](webrtc-software-solutions.md)
* [为什么阻止 WebRTC 并不能保护您免受检测](why-blocking-webrtc-doesnt-help.md)
* [我们的现场测试结果](field-test-results.md)
* [常见问题](../../faq-and-support/faq/)



### **介绍性理论**

现代反欺诈系统越来越坚持识别您的真实地址或检测隐藏您地址的工具的使用。即使您使用代理或 <mark style="color:purple;">VPN</mark>，他们也可以通过许多参数确定您不是“真实”用户。

最常见的检测机制之一是 <mark style="color:purple;">WebRTC</mark>，这是一种可以通过代理发送请求的技术，因此如果 <mark style="color:purple;">WebRTC</mark> 未被浏览器阻止，则会暴露您的真实 IP。<br>

解决方案是什么？代理和软件产品均支持双向 <mark style="color:purple;">UDP</mark> 协议。

{% hint style="info" %}
{% endhint %}

&#x20;



