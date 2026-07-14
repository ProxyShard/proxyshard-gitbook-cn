---
icon: magnifying-glass
---

# IP 检查器

<mark style="color:purple;">ProxyShard IP Checker</mark> 是一款免费工具，用于检查您的 IP 地址、地理位置、浏览器数据、WebRTC 泄漏和独特的浏览器配置文件质量得分。

{% embed url="https://proxyshard.com/ip-checker" %}

<figure><img src="../.gitbook/assets/image (41).png" alt="" width="563"><figcaption></figcaption></figure>

***

## 主要字段

### 我的IP

所有网站都能看到您当前的外部 IP 地址。旁边显示国旗和复制按钮。如果代理连接正确，这应该是 <mark style="color:purple;"> 代理服务器 IP</mark>，而不是您的真实地址。

### 浏览器分数

显示检测到的匿名问题数量的数字分数。 **越低越好。**

{% hint style="info" %}
单击 **“查看详细信息”** 查看每个参数的完整报告。
{% endhint %}

***

## 一般 IP 信息

### 提供者

拥有您的 IP 的互联网提供商 (ISP) 的名称。例如：`WYOCORE TECHNOLOGIES LLC`。如果您使用代理，此字段将显示代理服务器提供商。

### WebRTC IP

{% hint style="danger" %}
这是最重要的领域。如果显示 **“WebRTC 已泄露”**，则表示在代理处于活动状态时，您的真实 IP 对网站可见。更多详细信息：[WebRTC 泄漏的工作原理](about-udp/how-webrtc-leak-works.md)
{% endhint %}

<mark style="color:purple;">WebRTC</mark> 是用于 p2p 连接的浏览器协议。它可以绕过代理和 VPN 暴露真实的 IP。该字段显示 <mark style="color:purple;">WebRTC</mark> 检测到的 IP。如果它与 **我的 IP** 不同，则存在泄漏。

|状态 |这意味着什么 |
| ------------------- | ------------------------------------- |
| `WebRTC is leaked` |检测到泄漏；真实IP可见|
| `WebRTC is blocked` | WebRTC 被阻止；没有泄漏|
| _（空字段）_ |未检测到WebRTC；没有泄漏|

{% hint style="warning" %}
正常情况下，<mark style="color:purple;">WebRTC</mark> 应该显示代理 IP 地址本身。
{% endhint %}

### 假ISP

检查提供商是否是“假的”。这对于某些掩盖其来源的 VPN 服务来说很常见。 `No` 表示提供商是真实的。

### Host

您的 IP 的反向 DNS 记录（PTR 记录）。显示哪个域名链接到该地址。

### 匿名器

确定您的 IP 是否属于已知的匿名基础设施：VPN、代理或 Tor。 `No` 表示该 IP 未在匿名器数据库中列出。

***

## 浏览器状态报告

使用 **“查看详细信息”** 按钮打开。显示按严重性级别分组的详细浏览器和网络分析结果：

|水平|这意味着什么 |
| ------------ | -------------------------------------------------- |
| **关键** |严重泄漏；真实数据肯定曝光|
| **高** |严重问题；高去匿名化风险 |
| **中** |中等风险；可疑参数|
| **低** |风险低；轻微不匹配|
| **信息** |信息性；不影响匿名 |

### 检查参数

#### ISP / 连接类型

确定 IP 地址类型：`residential`（家庭）、`datacenter/hosting`（数据中心）或 `mobile`。数据中心地址被标记为 `medium`，因为它们很容易被具有严格反机器人策略的网站检测到。

> 示例：`ISP: IP 156.226.202.211 - datacenter/hosting (WYOCORE TECHNOLOGIES LLC), ASN AS214413`

{% hint style="info" %}
#### 这是数据中心代理的典型情况。如果您使用 ISP\Residential\Mobile 代理，此参数不应显示与数据中心相关的任何内容。
{% endhint %}

#### WebRTC 泄露

通过<mark style="color:purple;">WebRTC</mark> API检查浏览器是否暴露真实IP。如果检测到与代理不同的IP，则级别为`critical`。

#### 时区

将浏览器时区 (`Intl.DateTimeFormat`) 与 IP 地理位置进行比较。如果它们不匹配（例如，IP 来自德国，而浏览器显示 UTC+3），则表明使用了代理。

#### 语言

检查浏览器的`navigator.language`和`navigator.languages`。如果浏览器语言（例如，`ru-RU`）与IP国家/地区不匹配，反欺诈系统会注意到它。

#### 屏幕分辨率

分析屏幕分辨率和宽高比。非标准值可能表示虚拟机或无头浏览器。

#### 画布指纹

在页面上绘制隐藏元素并读取其像素哈希。每个设备的呈现方式都略有不同，从而创建了独特的指纹。修改过的或空的 Canvas 是反检测浏览器的标志。

#### WebGL / GPU

通过WebGL API读取显卡信息：`RENDERER`和`VENDOR`（例如`ANGLE (NVIDIA GeForce RTX...)`）。这可以暴露真实的硬件并帮助识别设备。

#### 音频指纹

通过 `AudioContext` 生成音频信号并读取其哈希值。它的工作原理与 Canvas 相同：它为每个设备创建唯一的指纹。反检测浏览器会替换该值。

#### 自动化/WebDriver

检查自动化指标：

* `navigator.webdriver` - 该标志由 Selenium、Puppeteer 和 Playwright 设置
* `chrome.runtime` 和其他 CDP 工件
* 非标准`window`属性

如果检测到，则级别为 `high` 或 `critical`。

#### 字体

通过 CSS 和 Canvas 检测已安装字体的列表。字体集对于每个操作系统和用户都是唯一的，即使 IP 发生变化也可用于识别。

#### Cookies/本地存储

检查浏览器中是否启用了 cookies 和 `localStorage`。禁用存储是一种非典型行为，通常出现在特殊配置中。

#### 请勿追踪 (DNT)

读取 `DNT` 标头值。它本身并不重要，但它是整个浏览器指纹的一部分。

#### 地理定位 API

检查 `navigator.geolocation` 是否可用以及它与 IP 地理位置的关联方式。无需请求确定地理位置的许可； API 的存在本身就已经提供了丰富的信息。

#### 硬件并发

`navigator.hardwareConcurrency` 是逻辑 CPU 核心数。非标准值（例如，`1`）是虚拟机的典型值。

#### 设备内存

`navigator.deviceMemory` 是以 GB 为单位的 RAM 量（四舍五入值）。与 `hardwareConcurrency` 一起，它有助于检测虚拟机或无头环境。

#### 平台

`navigator.platform` 是浏览器平台（`Win32`、`MacIntel`、`Linux x86_64`）。如果它与用户代理不匹配，则这是数据伪造的明显迹象。

#### 广告拦截器

通过尝试加载已知的广告脚本来检测广告拦截器（uBlock、AdGuard 等）。这是整体指纹配置文件的一部分。

#### 深色模式

读取 `prefers-color-scheme` - 深色或浅色操作系统主题。这是一个小但稳定的指纹参数。

#### 触摸/指针

检查 `navigator.maxTouchPoints` 和指针类型（`mouse`、`touch`、`pen`）。如果用户代理指示移动设备但未检测到触摸屏，则这是模拟的标志。

***

## 如何读取结果

{% hint style="success" %}
**一切都很好：**我的 IP = 代理 IP，WebRTC 未检测到或被阻止，浏览器分数 = 0，ISP 类型 = `residential`。
{% endhint %}

{% hint style="warning" %}
**数据中心/ISP 代理正常：** ISP 类型 = `datacenter/hosting`。这是预期的，对于大多数任务来说不是问题。
{% endhint %}

{% hint style="danger" %}
**问题：** 如果 WebRTC 显示的 IP 与代理不同，则必须立即修复泄漏。

我们强烈建议为所有任务使用通用设置：\
ISP 代理 + 良好的反检测浏览器。设置示例：[Vision](../setup-guides/antidetect-browsers/vision-browser.md)
{% endhint %}



