---
icon: lock-keyhole-open
---

# 为什么单独的 TCP 代理是不够的！

即使您的 SOCKS5 代理支持 <mark style="color:purple;">UDP</mark>，大多数反检测浏览器（尤其是基于 Chromium 的浏览器）也无法通过代理传递 <mark style="color:purple;">WebRTC</mark> 流量。原因是浏览器引擎的技术限制。

如今，验证码系统已经引入了对 <mark style="color:purple;">WebRTC</mark> 是否存在的增强检查。一个例子是 <mark style="color:purple;">Discord</mark>：他们连接了“<mark style="color:purple;">Hcaptcha-enterprise</mark>”，其中已经包含了对用户端启用的 <mark style="color:purple;">WebRTC</mark> 的检查。



