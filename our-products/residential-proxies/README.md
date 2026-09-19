---
icon: house-signal
---

# 住宅代理

<mark style="color:purple;">住宅代理</mark>托管在真实的家庭设备上。它们非常适合使用大量家庭宽带运营商的 IP，并支持精细定位，直至运营商级别。\
您可以[在此处](../restrictions.md)查看产品限制。

{% hint style="info" %}
未使用的流量不会在月底失效；它会保留在订单中，直到全部用完。
{% endhint %}

{% hint style="warning" %}
IP 地址来自真实的家庭宽带。如果池中的设备退出流量共享网络，会话可能随时切换。如果您需要**静态 IP**，请参阅 [Datacenter](../datacenter-proxies.md) 或 [ISP 代理](../isp-proxies.md)。
{% endhint %}

{% embed url="https://dashboard.proxyshard.com/en/residential-main" %}

购买和付款的分步说明：[购买住宅代理](../../site-navigation/buying-and-renewing/buying-residential-proxies.md)。

## 套餐

| 参数              | [Standard](standard-residential.md) | [Unlimited](unlimited-residential-proxy.md) | [Premium](premium-residential.md) |
| --------------- | ------------------------------------ | ------------------------------------------- | --------------------------------- |
| 池大小            | 300k - 400k                          | 300k - 400k (= Standard)                    | 3.8M - 4.6M                       |
| 最大连接数         | 35,000                               | 5,000                                       | -                                 |
| 最大速度           | 75 Mbps                              | 75 Mbps                                     | 75 Mbps                           |
| [UDP 支持](../about-udp/) | ✓（美国除外；受端口限制） | ✓（美国除外；受端口限制） | ✓（部分城市及 macOS/iOS 设备除外） |
| [Device OS 筛选](../p0f-spoofing.md) | ✗ | ✗ | ✓ |
| 无限套餐           | ✗                                    | ✓                                           | ✗                                 |
| 计费方式           | 按 GB（按量付费）                      | 日 / 半月 / 月                               | 按 GB（按量付费）                    |
| 价格              | **$2 / GB**                          | **$30** / 天 · **$399** / 半月 · **$699** / 月 | **$3 / GB**                  |

## 可用国家

### Standard 与 Unlimited Residential

共有 **165 个国家**，并提供 `Random` 选项以自动选择国家。

{% content-ref url="available-countries.md" %}
[available-countries.md](available-countries.md)
{% endcontent-ref %}

### Premium Residential

共有 **214 个国家**。

{% content-ref url="premium-available-countries.md" %}
[premium-available-countries.md](premium-available-countries.md)
{% endcontent-ref %}

## 如何购买

1. 在 `Residential Proxy` 中选择 `Standard`、`Residential Premium` 或 `Unlimited`。
2. 对于按流量计费的套餐，请输入所需的流量大小。
3. 如果有优惠码，请在 `Promocode` 中输入并点击 `Apply`。
4. 确认金额后点击 `Buy now`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/residential-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/residential-purchase-form_white.png" alt="购买住宅代理">
  </picture>
</figure>

订单付款和流量充值流程请参阅[购买住宅代理](../../site-navigation/buying-and-renewing/buying-residential-proxies.md)。

## 代理设置

一般情况下，只需选择 `Country` 并点击 `Generate proxy`。需要更精确的定位或会话控制时，再配置其他参数。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/residential-settings_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/residential-settings_white.png" alt="住宅代理设置">
  </picture>
</figure>

1. `Country` 用于选择国家。
2. `Region` 用于选择国家内的地区。
3. `City` 用于选择城市。
4. `ISP` 按运营商筛选地址。该字段仅适用于 [Premium Residential](premium-residential.md)。
5. `Session` 用于设置轮换方式。`Sticky` 在 `TTL` 范围内保持同一 IP，`Rotate` 则在每次请求时更换 IP。
6. `Protocol` 用于选择 `HTTP` 或 `SOCKS5`。
7. `Relay` 用于更换连接服务器。仅在出现连接问题时使用。
8. `TTL` 设置 `Sticky` 会话的 IP 有效时间，最小值为 60 秒。
9. `Device OS` 按设备操作系统筛选 [Premium Residential](premium-residential.md) 地址池。
10. `Amount` 设置每次生成的连接字符串数量。
11. `Session mode` 控制 Premium Residential 会话。`Default(after 5sec)` 会在设备超过五秒未响应时切换会话。`Static` 会在 `TTL` 范围内等待同一设备重新上线。
12. `Generate proxy` 根据所选参数生成连接字符串。
13. `Proxy List` 显示已生成的连接字符串。可通过 `Format` 选择格式，并通过 `Copy all` 复制完整列表。

`Presets` 用于保存可重复使用的设置组合。配置各字段后点击 `Save preset`，下次生成代理时即可直接选择已保存的预设。

{% hint style="warning" %}
同时使用 `Device OS`、城市和运营商筛选会大幅缩小可用地址池。在 Tier 2 和 Tier 3 国家，可能找不到符合条件的 macOS 或 iOS 设备。
{% endhint %}

{% hint style="warning" %}
使用非默认 `Session mode` 时，如果所选设备离线，连接字符串可能不再响应。遇到这种情况，请通过 `Generate proxy` 生成新的连接字符串。
{% endhint %}

{% hint style="danger" %}
`Regenerate password` 会更改订单密码，并立即使之前生成的所有连接字符串失效。仅在身份验证信息可能泄露时使用。要按用户查看流量，请使用 `Users` 选项卡。
{% endhint %}

`Proxy List` 是动态字段，不是存储空间。之前生成的连接字符串仍可继续使用，因为所选参数已写入 `Username`。如需保存设置，请使用 `Presets`。

## 连接字符串格式

标准格式如下：

```text
host:port:username:password
```

* `host` 指定连接服务器，例如 `relay-eu.proxyshard.com`。
* `port` 用于连接服务器，本身不会决定最终 IP。
* `username` 包含定位参数和会话标识符 `sid`。
* `password` 用于身份验证。

完整的连接字符串可添加到浏览器、应用程序或其他客户端。具体步骤请参阅[设置指南](../../setup-guides/getting-started.md)。

## 统计信息

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/residential-statistics_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/residential-statistics_white.png" alt="住宅代理统计信息">
  </picture>
</figure>

1. 打开 `Statistics` 选项卡。
2. 为 `Traffic Statistics` 图表选择时间范围。
3. 单独为 `Requests Statistics` 表格选择时间范围。

新数据可能会延迟 10-20 分钟显示。统计数据保留一个月。

## 适用于哪些任务

社交网络与多账户管理、加密货币交易所（Binance、Bybit 等）、Polymarket、网页抓取、SEO 监控、广告验证（ad verification）、电商分析、价格监控、地理定向网站测试。

## 住宅代理的优缺点

#### <mark style="color:green;">优点：</mark>

* **灵活计费** - 按量付费或无限订阅（Unlimited）
* **更换 IP** - 按需或按计时器（TTL）轮换地址
* **广泛的地理定位** - 可选择国家、地区、城市和运营商
* **家庭来源地址** - IP 注册在家庭宽带运营商名下
* **UDP 支持** - Standard、Unlimited 和 Premium 均可用，但需遵守各产品的限制

#### <mark style="color:red;">缺点：</mark>

* **可能出现速度下降** - 取决于终端设备的网络质量，这是该产品的特性
* **动态 IP** - 地址可能随时被切换；如需静态 IP，请参阅 [ISP](../isp-proxies.md) 或 [Datacenter](../datacenter-proxies.md)
* **不支持 p0f 伪装** - Premium Residential 仅提供 [Device OS 筛选](../p0f-spoofing.md)
* **UDP 限制** - Standard 和 Unlimited 在美国不支持 UDP；Premium 的部分城市及 macOS/iOS 设备不支持 UDP。此外还需遵守通用的[端口限制](../restrictions.md)

{% hint style="success" %}
需要支持 UDP 的静态地址？请选择 [ISP 代理](../isp-proxies.md)。
{% endhint %}

{% hint style="info" %}
代理配置说明请参阅[设置指南](../../setup-guides/getting-started.md)。
{% endhint %}
