---
icon: git-alt
---

# 用于启用 WebRTC 的软件解决方案

#### 完整的 WebRTC 操作需要支持 UDP ASSOCIATE 的软件。

不同操作系统支持的软件示例：

<mark style="color:purple;">**反检测浏览器：**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/vision-browser.md) - 支持完整的 UDP 操作和工作 QUIC。

{% embed url="https://docs.proxyshard.com/cn/usage-instructions/antidetect-browsers/vision-browser" %}

{% hint style="success" %}
目前，我们的[ISP代理](https://dashboard.proxyshard.com/en/isp-proxy)和[Vision](../../setup-guides/antidetect-browsers/vision-browser.md)浏览器的组合是使用UDP代理最相关和最正确的设置。 ISP 代理还支持 p0f 修改，这使得任何参数都无法进行代理检测！
{% endhint %}

<mark style="color:purple;">**Windows：**</mark>

* ProxiFyre + Windows 数据包过滤器
* Win2Socks
* 网络
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)
* Proximac（已过时）

<mark style="color:purple;">**Linux:**</mark>

* proxychains-NG + go-tun2socks
* 红袜-ng

<mark style="color:purple;">**安卓：**</mark>

* 安卓版冲突
* 袜子机器人
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)

<mark style="color:purple;">**安卓：**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
您可以在[设置指南](../../setup-guides/getting-started.md)中查看当前列表，该列表不断更新。
{% endhint %}


