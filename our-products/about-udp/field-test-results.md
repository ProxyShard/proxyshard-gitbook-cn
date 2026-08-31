---
icon: island-tropical
---

# 我们的实测结果

我们在所有 [<mark style="color:purple;">**Datacenter**</mark>](../datacenter-proxies.md) 代理位置启用了 <mark style="color:purple;">**UDP**</mark>，并使用 [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) 浏览器进行了测试。结果如下：

* Google：连续创建 15 个账号，没有出现错误，也不需要手机号验证。
* Discord：注册以及加入启用了严格机器人检查的服务器均成功，包括通常会阻止 ISP 代理的服务器。
* Twitter：包含 10 张图片的 CAPTCHA 验证成功，后续重新验证也顺利完成。
* Facebook、Instagram 和 Facebook Ads：注册过程没有出现问题，也没有 CAPTCHA。

相比之下，通过不支持 **UDP** 的 ISP 代理执行相同操作时会出现错误，或需要短信验证。

在这些测试中，WebRTC 正确工作后，没有再出现误判机器人活动的问题。
