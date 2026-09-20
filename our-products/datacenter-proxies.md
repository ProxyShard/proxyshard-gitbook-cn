---
icon: server
---

# 数据中心代理

<mark style="color:purple;">数据中心代理</mark>适合高负载任务。代理部署在数据中心，可提供出色的速度和稳定性。

<mark style="color:purple;">数据中心代理</mark>与 <mark style="color:purple;">ISP</mark> 代理一样，每个地址仅分配给一名用户，不存在隐藏共享。这些地址均为 <mark style="color:purple;">IPv4</mark>，并支持 <mark style="color:purple;">UDP</mark>。

{% embed url="https://dashboard.proxyshard.com/en/datacenter-proxy" %}

购买和付款的分步说明：[购买 ISP / 数据中心代理](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md)。

当前产品限制请参阅[限制](restrictions.md)页面。

## 特性

| 参数              | 值                                                                        |
| --------------- | ------------------------------------------------------------------------- |
| IP 类型           | IPv4                                                                      |
| 共享              | 否 - 一个 IP 对应一个用户                                                   |
| 连接数限制         | 每个 IP 2,500                                                              |
| [UDP 支持](about-udp/) | ✓                                                                    |
| [p0f 支持](p0f-spoofing.md) | ✓（按月起租时，+$0.3 / IP）                                       |
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

## 如何购买

1. 打开 `Datacenter Proxy`。
2. 在 `Proxy region` 中选择国家或地区。
3. 在 `Billing cycle` 中选择租用周期。
4. 在 `Number of proxies` 中输入代理数量。
5. 如需自动续订订单，请启用 `Auto renew`。
6. 如有需要，请启用 `Enable p0f settings`。
7. 在 `Total slots` 中输入需要使用 p0f 伪装的代理数量。
8. 如有优惠码，请在 `Promocode` 中输入并点击 `Apply`。
9. 确认金额后点击 `Buy now`。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/datacenter-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/datacenter-purchase-form_white.png" alt="购买数据中心代理">
  </picture>
</figure>

付款和续订步骤请参阅[购买 ISP / 数据中心代理](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md)。

{% hint style="info" %}
付款后请等待 1-2 分钟，订单同步完成后代理即可使用。
{% endhint %}

## 订单字段

<figure>
  <picture>
    <source srcset="../.gitbook/assets/datacenter-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/datacenter-order-details_white.png" alt="数据中心代理订单字段">
  </picture>
</figure>

* `Status` 显示订单状态：`Active`、`On-hold` 或 `Canceled`。
* `Product tag` 用于添加标签，方便在产品列表中查找订单。
* `User ID` 用于系统内部识别订单，联系支持时可能需要提供。
* `Proxy Region` 显示所选国家或地区。
* `p0f slots` 显示当前启用的 p0f 槽位数量，以及下一计费周期的变更。
* `Username` 和 `Password` 是代理凭据。点击 `Regenerate` 会生成新密码，已有代理连接字符串将失效。
* `Billing cycle`、`Next due date`、`Price` 和 `Next charge` 显示租用周期及下次付款信息。
* `Auto-renew proxy` 用于控制自动续订，也可以通过 `Manage renewal` 调整相同设置。
* `p0f` 和 `Buy p0f slots` 分别用于打开指纹伪装设置和购买额外槽位。
* 在 `Proxy List` 中可以选择 `HTTP` 或 `SOCKS5`、更改连接字符串格式、使用 `Copy all` 复制列表，或通过 `Export All` 下载列表。

{% hint style="danger" %}
状态为 `Canceled` 的订单无法恢复。订单欠费三天后会进入该状态。
{% endhint %}

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
代理配置说明请参阅[设置指南](../setup-guides/getting-started.md)。
{% endhint %}

