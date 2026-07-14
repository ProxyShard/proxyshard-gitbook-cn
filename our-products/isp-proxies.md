---
icon: fire
---

# ISP 代理

<mark style="color:purple;">ISP 代理</mark> 与<mark style="color:purple;">Datacenter</mark> 代理一样，仅发布给一名用户：不共享，意味着每个地址不超过一个用户，并且没有隐藏共享。地址为 <mark style="color:purple;">IPv4</mark> 并支持 <mark style="color:purple;">UDP</mark>。

<mark style="color:purple;">ISP 代理</mark> 结合了 <mark style="color:purple;">Residential</mark> 代理和 <mark style="color:purple;">Datacenter</mark> 代理的优点。它们与 <mark style="color:purple;">Datacenter</mark> 代理一样稳定和静态，但它们使用注册到家庭互联网提供商的 IP 地址，例如 <mark style="color:purple;">Residential</mark> 代理。

这使它们成为处理 Tier-1 网站以及对 <mark style="color:purple;">IP</mark> 类型敏感的服务的最佳选择之一。有了 <mark style="color:purple;">UDP</mark> 的支持，它们几乎无法被检测到。\
\
<mark style="color:purple;">ISP</mark> 代理的最新更新添加了切换指纹的功能 (<mark style="color:purple;">p0f</mark>)。

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

## 特性

| 参数              | 值                                   |
| --------------- | ------------------------------------ |
| IP 类型           | IPv4（家庭宽带运营商）                |
| 共享              | 否 — 一个 IP 对应一个用户             |
| UDP 支持          | ✓                                    |
| p0f 支持          | ✓（+$0.6 / IP 每月）                  |
| 价格              | **$2** / IP 每月                      |

## 可用位置

| 国家 |
| ------ |
| 🇹🇷 土耳其 |
| 🇺🇸 美国 |
| 🇨🇿 捷克 |

{% hint style="info" %}
位置列表正在不断扩充。
{% endhint %}

## **它们如何工作？**

在订单中，您可以找到几个重要的项目和选项。让我们回顾一下它们：

您可以在[ISP代理](https://dashboard.proxyshard.com/en/isp-proxy)页面购买。在那里，您需要指定 <mark style="color:purple;">Country</mark>、<mark style="color:purple;">Rental period</mark> 和 <mark style="color:purple;">Quantity</mark>。如果需要，您可以开启<mark style="color:purple;">自动续费</mark>进行自动续费。

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
购买后，代理会在 1-2 分钟内开始工作，因为数据库需要与代理服务器同步。
{% endhint %}

## 订单字段说明

让我们回顾一下 <mark style="color:purple;">Order</mark> 字段：

<mark style="color:purple;">用户 ID</mark> - 该用户 ID 用于内部订单识别。有时，当您联系技术支持时，我们会要求您提供此信息。

<mark style="color:purple;">Status</mark> - 订单状态。可能的状态：

* <mark style="color:green;">**有效**</mark> - 有效订单
* <mark style="color:orange;">**保留**</mark> - 租赁期满后等待付款
* <mark style="color:red;">**已取消**</mark> - 已取消订单

{% hint style="danger" %}
状态为“<mark style="color:$danger;">**已取消**</mark>”的订单**在租赁期结束三天后**无法恢复**。
{% endhint %}

<mark style="color:purple;">Price</mark> - 每月产品价格

<mark style="color:purple;">用户名</mark> - 代理登录

<mark style="color:purple;">Password</mark> - 代理密码

<mark style="color:purple;">下一个到期日</mark> - 下一个收费日期

<mark style="color:purple;">复制代理</mark> - 用于将代理复制到剪贴板的按钮

<mark style="color:purple;">HTTP/SOCKS</mark> - 代理协议类型选择

<mark style="color:purple;">重新生成</mark> - 更改代理密码

<mark style="color:purple;">自动续订</mark> - 启用/禁用每月产品续订的切换 <mark style="color:purple;">（资金在购买时指定的日期从帐户余额中扣除）</mark>

## 适用于哪些任务

任何加密货币交易所、Polymarket、稳定的网页抓取会话、SEO 监控、电商价格监控、市场平台核查、广告验证（ad verification）、品牌监控、从家庭运营商 ASN 进行的网站测试、登录与用户场景的 QA、网站可用性监控、账户管理。

## ISP 代理的优缺点

#### <mark style="color:green;">优点：</mark>

* **真实的 ISP 地址** — IP 登记在真实的家庭互联网运营商名下（在地理定位数据库中 ASN 类型为运营商，而非托管）
* **可靠的家庭通信运营商**
* **宽带通道、延迟极低**
* **专属静态地址** — 整个租期内 IP 不变
* **支持 p0f 和 UDP**

#### <mark style="color:red;">缺点：</mark>

* **价格** — 高于数据中心代理
* **可用位置数量** — 与真实运营商的对接极其复杂，但我们在不断扩充列表

{% hint style="info" %}
您可以在我们的[设置指南](../setup-guides/getting-started.md)部分了解如何配置代理。
{% endhint %}


