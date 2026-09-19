---
icon: check-to-slot
---

# 如何检查 WebRTC 泄漏

您可以使用 ProxyShard IP Checker 或第三方服务 Ipbinding 检查 WebRTC。建议先使用我们的工具，它会在同一份报告中显示外部 IP、WebRTC 地址和 UDP 测试结果。

## 1. ProxyShard IP Checker

{% embed url="https://proxyshard.com/ip-checker" %}

### 正常结果

配置正确时，`My IP address` 与 `WebRTC IP` 应一致。这表示 WebRTC 使用的是代理地址，UDP 流量没有绕过代理连接。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/ip-checker-overview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/ip-checker-overview_white.png" alt="正确的 WebRTC 检查结果">
  </picture>
</figure>

### 未收到 UDP 候选地址

如果 `WebRTC IP` 显示 `error`，并且 `WebRTC Check` 区域显示 `No UDP candidates received`，说明浏览器没有收到 UDP 候选地址。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/webrtc-check-failed_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/webrtc-check-failed_white.png" alt="未收到 UDP 候选地址的 WebRTC 检查">
  </picture>
</figure>

{% hint style="warning" %}
该结果本身并不代表 IP 泄漏。WebRTC 可能被阻止，或者所选产品或应用程序无法传输 UDP。请查看[哪些产品支持 UDP](./README.md#ge-chan-pin-de-udp-zhi-chi-qing-kuang)，并使用[支持 UDP ASSOCIATE 的软件](webrtc-software-solutions.md)。
{% endhint %}

{% hint style="danger" %}
如果 `WebRTC IP` 与 `My IP address` 不同，说明 WebRTC 绕过了代理。此结果表示存在泄漏。
{% endhint %}

各字段的详细说明请参阅 [IP Checker](../ip-checker.md)。

## 2. Ipbinding

[Ipbinding](https://ipbinding.online/) 也会显示 WebRTC 候选地址。判断方式相同，WebRTC 地址应与代理地址一致。

{% embed url="https://ipbinding.online/" %}

