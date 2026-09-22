---
icon: fingerprint
---

# 网络指纹伪装 (p0f)

## p0f 是什么以及它为何重要

网络中的每台设备在 <mark style="color:$primary;">TCP/IP</mark> 层面都有自己的数字指纹，称为 <mark style="color:$primary;">**p0f**</mark> 指纹。它由网络协议栈参数构成，包括 MSS、TSval、TTL、TCP options、Window size 和 TOS 等。Windows、macOS、Linux、iOS 和 Android 的这些参数并不相同，反欺诈系统可以利用这种差异识别设备环境。

网站通常会进行以下检查：

1. 网站会检查 <mark style="color:$primary;">**User-Agent**</mark>、<mark style="color:$primary;">**TLS 指纹**</mark>和其他客户端参数，以判断用户使用的操作系统。
2. 同时，网站还会分析连接的<mark style="color:$primary;">**网络层**</mark>信息，也就是代理服务器随流量发送的 <mark style="color:$primary;">TCP/IP 指纹</mark>。
3. 如果浏览器显示 Windows 11，而 TCP/IP 指纹却对应 <mark style="color:$primary;">Linux</mark>，反欺诈系统就可能发现两者不一致。

**常见问题：** Datacenter 和 ISP 代理通常运行在 Linux 服务器上。如果不修改网络指纹，即使用户使用 Windows 或 macOS，TCP/IP 指纹仍可能显示为 Linux。反欺诈系统可能将这种不一致视为使用代理的迹象。

## ProxyShard 如何解决这个问题

ProxyShard 支持直接在控制面板中修改 p0f 指纹。选择目标操作系统后，代理服务器会使用与该系统相符的 TCP/IP 参数发送数据包。

可用的伪装选项：

| 值 | 描述 |
| --- | --- |
| **Unset** | 默认指纹（Linux） |
| **Windows 10** | Windows 10 指纹 |
| **Windows 11** | Windows 11 指纹 |
| **Mac OS** | macOS 指纹 |
| **Linux** | Linux 指纹 |
| **iOS** | iOS 指纹 |
| **Android** | Android 指纹 |

### ISP 和数据中心代理

打开订单，点击 `p0f`，然后为每个 IP 选择所需的操作系统。ISP 和数据中心代理的设置方式相同。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-datacenter-isp_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-datacenter-isp_white.png" alt="ISP 和数据中心代理的 p0f 设置">
  </picture>
</figure>

### 移动代理

在 `Signature` 字段中选择代理应使用的操作系统指纹。更改设置后，点击 `Restart` 重启代理。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-mobile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-mobile_white.png" alt="为移动代理选择网络指纹">
  </picture>
</figure>

部分移动代理地区暂不支持 p0f 伪装。当前列表请参阅[限制](restrictions.md)。

### Premium Residential

在 Premium Residential 中，`Device OS` 参数会按设备操作系统筛选代理池。该功能用于筛选代理池，不会伪装网络指纹。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-premium-residential_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-premium-residential_white.png" alt="按 Device OS 筛选 Premium Residential 代理">
  </picture>
</figure>

`Device OS` 的可用性取决于地区。详情请参阅[限制](restrictions.md)。

{% hint style="warning" %}
更改 p0f 前，请关闭所有通过该代理建立的连接。旧连接仍会使用原来的指纹，并可能影响新设置生效。修改后请等待 2-3 分钟，再重新连接。
{% endhint %}

## 真实结果

初步测试表明，p0f 伪装可以提高反欺诈检查的通过率。以下是一个已经验证的场景：

{% hint style="success" %}
**Google 账号：** 我们与 [Vision Browser](../setup-guides/antidetect-browsers/vision-browser.md) 开发者测试了在不修改浏览器指纹的情况下注册 Google 账号。使用全新配置文件且未启用 p0f 伪装时，系统会立即要求通过二维码验证。将 p0f 指纹设置为 Windows 10 或 Windows 11 后，二维码验证不再出现，Google 改为要求手机号验证。这表明浏览器环境与网络指纹之间的不一致已被消除。
{% endhint %}

注册 Google 账号时，如果浏览器环境与网络指纹不一致，桌面端通常会触发二维码验证。p0f 伪装可以让网络指纹与所选操作系统保持一致。

## 推荐堆栈

为了获得最佳效果，我们建议使用：

* [**Vision Browser**](../setup-guides/antidetect-browsers/vision-browser.md)，一款支持 UDP 的反检测浏览器
* **启用 p0f 伪装的 ProxyShard ISP 代理**

在这种组合中，Vision Browser 负责浏览器指纹，p0f 负责网络层指纹，ISP 代理则提供住宅网络运营商的 IP 地址。

## 支持情况

p0f 伪装和设备筛选适用于以下产品：

* [数据中心代理](datacenter-proxies.md)
* [ISP 代理](isp-proxies.md)
* [移动代理](mobile-proxies.md)
* [Premium Residential](residential-proxies/premium-residential.md) - 通过 [Device OS](residential-proxies/#dai-li-she-zhi) 参数筛选设备，不提供 p0f 伪装

{% hint style="warning" %}
p0f 伪装在某些[移动代理](mobile-proxies.md)上不可用。请参阅[限制](restrictions.md)页面上的完整限制列表。
{% endhint %}
