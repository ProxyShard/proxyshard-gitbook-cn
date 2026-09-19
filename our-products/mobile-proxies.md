---
icon: signal
---

# 移动代理

<mark style="color:purple;">移动代理</mark>托管在配备真实 SIM 卡的路由器上。其连接的类型和质量与通过移动运营商的普通移动互联网完全相同 - 就像您手机上的网络一样。支持 <mark style="color:purple;">UDP</mark>，并提供丰富的地点和运营商选择。

{% hint style="info" %}
**移动代理可在任何设备上工作。** “移动”一词仅指通过 SIM 卡连接的方式，而非终端设备的类型。无论是在 PC、笔记本还是反检测浏览器中，都同样好用。
{% endhint %}

{% hint style="warning" %}
**这是一款专业产品 - 面向了解其用途的用户。** 流量经由真实 SIM 卡传输，因此速度可能波动 - 这是正常现象，而非故障。如果不确定移动代理是否适合您的任务，请在 [live 聊天](../contact-us.md)中咨询，或考虑 [ISP 代理](isp-proxies.md)（速度稳定、家庭 IP）或[住宅代理](residential-proxies/README.md)（庞大的池、海量会话）。
{% endhint %}

{% hint style="danger" %}
1\) 设备指纹切换 (p0f) 并非在所有运营商中都可用。请参阅[限制](restrictions.md)页面上的完整限制列表。

2\) 不使用 VPN 的俄罗斯用户不可用。
{% endhint %}

{% embed url="https://dashboard.proxyshard.com/en/mobile-proxy" %}

购买和激活的分步说明：[购买移动代理](../site-navigation/buying-and-renewing/buying-mobile-proxies.md)。

## 特性

| 参数              | 值                                     |
| --------------- | ------------------------------------- |
| IP 类型           | 移动 IPv4                              |
| 共享              | 否 - 一个端口对应一个用户               |
| 流量              | 无限                                   |
| [UDP 支持](about-udp/) | ✓                               |
| [p0f 支持](p0f-spoofing.md) | ✓（并非所有位置可用，见上文）  |
| 价格              | 从 **$4** / 天 · 从 **$55** / 月        |

## 可用位置

| 国家 | 运营商 |
| ------ | --------- |
| 🇺🇸 美国 | T-Mobile (5G)、Verizon (5G, Colorado) |
| 🇬🇧 英国 | O2、Vodafone |
| 🇩🇪 德国 | O2、Vodafone |
| 🇫🇷 法国 | SFR (5G)、Bouygues Telecom (5G) |
| 🇮🇹 意大利 | Vodafone (5G)、WindTre (5G) |
| 🇪🇸 西班牙 | Digimobil、Movistar (5G)、Vodafone (5G) |
| 🇵🇹 葡萄牙 | NOS (5G) |
| 🇳🇱 荷兰 | Ziggo (5G)、Odido (5G) |
| 🇮🇪 爱尔兰 | Vodafone (5G)、Three (5G) |
| 🇵🇱 波兰 | T-Mobile (5G) |
| 🇺🇦 乌克兰 | Lifecell、Vodafone、Kyivstar |
| 🇲🇩 摩尔多瓦 | Moldcell、Moldtelecom |
| 🇨🇦 加拿大 | Rogers |
| 🇮🇩 印度尼西亚 | Telkomsel |

{% hint style="info" %}
列表会定期扩充。最新位置与价格请见 [Mobile proxy](https://dashboard.proxyshard.com/en/mobile-proxy) 购买页面。
{% endhint %}

## 如何购买

1. 打开 `Mobile Proxy`。
2. 通过 `Country filter` 选择国家。
3. 在所需运营商的卡片中选择租用期限。
4. 点击 `Buy`。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/mobile-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/mobile-purchase-form_white.png" alt="购买移动代理">
  </picture>
</figure>

付款、首次激活和续费流程请参阅[购买移动代理](../site-navigation/buying-and-renewing/buying-mobile-proxies.md)。

## 订单字段与管理

<figure>
  <picture>
    <source srcset="../.gitbook/assets/mobile-order-settings_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/mobile-order-settings_white.png" alt="移动代理订单字段">
  </picture>
</figure>

1. `Signature` 用于选择网络签名。可选值包括 `w`、`w10`、`w7`、`linux`、`android`、`macos` 和 `ios`。更改签名后，请务必点击 `Restart`。
2. `Auto-reset` 按所选时间间隔自动重启连接。
3. `Restart` 用于激活端口或更换 IP。也可以通过专属 `Reset URL` 执行相同操作。
4. `Auto renew` 在余额充足时自动续费订单。
5. `Re-generate credentials` 用于生成新的身份验证信息。执行后，旧的代理连接字符串将失效。

其他字段：

* `Product tag` 用于添加标签，方便在列表中查找订单。
* `Proxy info` 显示国家、运营商和套餐类型。
* `Order status` 显示订单状态：`Active`、`On-hold` 或 `Canceled`。
* `Proxy status` 显示端口状态：`Active` 或 `Disconnected`。
* `Username` 和 `Password` 为身份验证信息。
* `Billing cycle`、`Next due date` 和 `Price` 显示租用期限和下次付款信息。
* 在 `Proxy List` 中，可以选择连接字符串格式，通过 `Copy all` 复制列表，或通过 `Export All` 下载列表。

{% hint style="warning" %}
购买后以及端口连续三小时无活动后，需要通过 `Restart` 或 `Reset URL` 激活端口。当 `Proxy status` 显示 `Disconnected` 时，代理无法使用。
{% endhint %}

## 适用于哪些任务

社交网络与多账户管理、移动广告验证（mobile ad verification）、移动广告核查、大多数加密货币交易所、Polymarket、移动网站与应用测试、移动版网站抓取、移动搜索结果 SEO 监控、电商移动价格监控、地理定向内容测试、移动资费的旅行类抓取、移动环境下的品牌监控。

## 移动代理的优点和缺点

#### <mark style="color:green;">优点：</mark>

* **可选择具体运营商** - 通过所需的移动运营商接入
* **通过 Reset URL 更换 IP** - 轮换频率不超过每分钟一次
* **支持 p0f** - 大多数位置可用（见[限制](restrictions.md)）
* **支持 UDP**
* **灵活的租期** - 从一天到一个月
* **专属端口** - 一张 SIM 卡，一个用户

#### <mark style="color:red;">缺点：</mark>

* **可能出现速度下降** - 当运营商基站过载时 - 少见，但有可能
* **对新手而言较复杂的产品** - 建议购买前先在[支持](../contact-us.md)处咨询
* **在 macOS / iOS 上切换 p0f** 会因算法复杂而降低通道速度
* **动态 IP** - 地址可能随时由运营商主动切换
* **同时只能一个会话** - 一个端口保持一个 IP。如果需要_同时_连接多个设备（不是轮流，而是在同一时刻），请购买单独的端口或考虑[住宅代理](residential-proxies/README.md)

{% hint style="info" %}
代理配置说明请参阅[设置指南](../setup-guides/getting-started.md)。
{% endhint %}

