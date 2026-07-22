---
icon: server
---

# 数据中心代理

<mark style="color:purple;">数据中心代理</mark> 是高负载场​​景和任务的代理。它们通常托管在数据中心并提供最高的速度和稳定性。

<mark style="color:purple;">数据中心代理</mark>与<mark style="color:purple;">ISP</mark>代理一样，仅发布给一名用户：不共享，意味着每个地址不超过一个用户，并且没有隐藏共享。地址为 <mark style="color:purple;">IPv4</mark>，还支持 <mark style="color:purple;">UDP</mark>。

{% embed url="https://dashboard.proxyshard.com/en/datacenter-proxy" %}

## 特性

| 参数              | 值                                                                        |
| --------------- | ------------------------------------------------------------------------- |
| IP 类型           | IPv4                                                                      |
| 共享              | 否 - 一个 IP 对应一个用户                                                   |
| 连接数限制         | 每个 IP 2,500                                                              |
| UDP 支持          | ✓                                                                         |
| p0f 支持          | ✓（按月起租时，+$0.3 / IP）                                                 |
| 价格              | **$0.3** / 3 天 · **$0.4** / 周 · **$0.7** / 半月 · **$1.2** / 月          |

## 可用位置

* 🇩🇪 德国
* 🇫🇷 法国
* 🇬🇧 英国
* 🇲🇩 摩尔多瓦
* 🇳🇱 荷兰
* 🇵🇱 波兰
* 🇺🇦 乌克兰
* 🇪🇸 西班牙

## **它们如何工作？**

在订单中，您可以找到几个重要的项目和选项。让我们回顾一下它们：

您可以在[数据中心代理](https://dashboard.proxyshard.com/en/datacenter-proxy)页面购买。在那里，您需要指定 <mark style="color:purple;">Country</mark>、<mark style="color:purple;">Rental period</mark> 和 <mark style="color:purple;">Quantity</mark>。如果需要，您可以开启<mark style="color:purple;">自动续费</mark>进行自动续费。

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
购买后，代理会在 1-2 分钟内开始工作，因为数据库需要与代理服务器同步。
{% endhint %}

## 订单字段说明

让我们回顾一下 <mark style="color:purple;">Order</mark> 字段：

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

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

大多数加密货币交易所、Polymarket 及交易平台，对简单站点的大规模网页抓取，公共数据的快速采集，可用性与正常运行时间检测，SEO 抓取，对防护较弱站点的价格监控，对自有系统的负载测试，目录与名录解析，API 请求自动化。

## 数据中心代理的优缺点

#### <mark style="color:green;">优点：</mark>

* **Tier 4 数据中心的宽带通道**，延迟尽可能低
* **专属静态地址** - 整个租期内 IP 不变
* **支持 p0f 和 UDP**
* **价格低廉** - 所有产品中最实惠的选项
* **灵活的租期** - 从 3 天到一个月
* **高稳定性与可用性**

#### <mark style="color:red;">缺点：</mark>

* **容易被识别** - 在主流地理定位数据库中标记为 DC / Hosting，这很正常，我们也不掩饰
* **不适用于部分平台** - 一些资源直接屏蔽 DC 地址（例如 DePIN 项目 Grass 和 Gradient）

{% hint style="success" %}
这些限制可通过 [ISP 代理](isp-proxies.md)绕过。
{% endhint %}

{% hint style="info" %}
您可以在我们的[设置指南](../setup-guides/getting-started.md)部分了解如何配置代理。
{% endhint %}

