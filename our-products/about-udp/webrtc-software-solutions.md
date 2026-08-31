---
icon: git-alt
---

# 启用 WebRTC 的软件方案

#### 要完整使用 WebRTC，软件必须支持 UDP ASSOCIATE。

不同操作系统上的可用软件示例：

<mark style="color:purple;">**反检测浏览器：**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/vision-browser.md)：一款价格合理且可靠的付费浏览器，支持 UDP、QUIC、Smart Fingerprint 及其他实用功能。我们网站上超过 60% 的团队选择使用它。

{% hint style="success" %}
将我们的 [ISP Proxy](https://dashboard.proxyshard.com/en/isp-proxy) 与 [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) 浏览器配合使用，是通过代理传输 UDP 的推荐方案之一。ISP Proxy 还支持更改 [p0f](../p0f-spoofing.md) 网络指纹。
{% endhint %}

* [<mark style="color:$tint;">ShardX</mark>](../shardx-launcher.md)：我们的开源解决方案，提供丰富的配置文件，并正确支持 UDP 和 QUIC。

<mark style="color:purple;">**Windows：**</mark>

* ProxiFyre + Windows Packet Filter
* Win2Socks
* Netch
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS：**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)

<mark style="color:purple;">**Linux：**</mark>

* proxychains-NG + go-tun2socks
* redsocks-ng

<mark style="color:purple;">**Android：**</mark>

* Clash for Android
* SocksDroid
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)
* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
最新的软件列表请参阅[使用说明](../../setup-guides/getting-started.md)。
{% endhint %}
