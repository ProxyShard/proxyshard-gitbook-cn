---
description: 关于产品、连接以及服务运作的常见问题
icon: circle-question
---

# 常见问题

{% hint style="warning" %}
**信息截至 2026 年 6 月有效。** 产品、地区、运营商和价格的列表可能发生变化，购买前请在[控制面板](https://dashboard.proxyshard.com/)上确认最新信息。
{% endhint %}

***

## 1. 哪些产品支持 p0f 伪装或操作系统筛选？

网络指纹伪装（<mark style="color:purple;">p0f</mark>）或按操作系统筛选设备可在以下产品中使用：

* [**Premium Residential**](../../our-products/residential-proxies/premium-residential.md) - Device OS 筛选
* [**Datacenter**](../../our-products/datacenter-proxies.md) 代理 - p0f 伪装
* [**ISP**](../../our-products/isp-proxies.md) 代理 - p0f 伪装
* [**Mobile**](../../our-products/mobile-proxies.md) 代理 - p0f 伪装，但并非所有运营商均支持

移动代理的运营商限制请参阅[移动代理页面](../../our-products/mobile-proxies.md)。

[Standard Residential](../../our-products/residential-proxies/standard-residential.md) 和 [Unlimited Residential](../../our-products/residential-proxies/unlimited-residential-proxy.md) 均不支持 p0f 伪装或 Device OS 筛选。

技术详情：[网络指纹伪装 (p0f)](../../our-products/p0f-spoofing.md)。

***

## 2. 哪些产品支持 UDP？

UDP 在**所有**产品上都受支持，但以下情况除外：

* 位于 <mark style="color:purple;">**美国**</mark> :flag\_us: 的**住宅代理**和**无限住宅代理**（自 2026 年初起，美国运营商方面的限制）
* **所有地区**的**高级住宅代理**

在 Datacenter、ISP、Mobile 以及非美国住宅代理上，UDP 正常工作。

详情：[关于 UDP 协议](../../our-products/about-udp/)。

***

## 3. 是否支持 QUIC？

是的，**QUIC 在所有支持 UDP 的代理上均受支持**（请参阅问题 2）。但您的软件也必须能够处理 QUIC。

例如在 [Vision 浏览器](../../setup-guides/antidetect-browsers/vision-browser.md) 中，需要在设置中启用 <mark style="color:purple;">**Enable QUIC**</mark> 选项。

***

## 4. 哪些代理是静态的（IP 不变）？

完全**静态**（在整个租用期间 IP 不变）的代理只有：

* <mark style="color:purple;">**Datacenter**</mark> 代理
* <mark style="color:purple;">**ISP**</mark> 代理

住宅代理和移动代理本质上是轮换型的，其 IP 在使用过程中会发生变化（请参阅下面的问题 11 和 14）。

***

## 5. 哪些产品是独享的（一个订单 = 一个用户）？

无共享、独享出售的产品：

* <mark style="color:purple;">**Datacenter**</mark> 代理 - 一个 IP 对应一个用户
* <mark style="color:purple;">**ISP**</mark> 代理 - 一个 IP 对应一个用户
* <mark style="color:purple;">**Mobile**</mark> 代理 - 一个端口（一张 SIM 卡）对应一个用户

住宅代理通过共享地址池工作，并非独享。

***

## 6. 刚购买 / 续费了 Datacenter 或 ISP，但代理无法使用

购买或续费 Datacenter / ISP 订单后，需要 **1-2 分钟**将订单与代理服务器同步。如果过了几分钟代理仍无响应，请联系我们的[支持](../../contact-us.md)。

***

## 7. Datacenter / ISP 代理的续费窗口是多久？

Datacenter 和 ISP 代理仅可在租用期结束后的 **3 天内**续费。

{% hint style="danger" %}
如果 3 天内未续费，**订单将被永久删除**。之后将无法恢复同一 IP 地址或订单。
{% endhint %}

我们建议在订单设置中启用 <mark style="color:purple;">**Auto renew**</mark> 选项，让续费自动从您的余额中扣除。

***

## 8. 刚购买了移动代理，但代理无法使用

购买移动代理后，需要通过以下方式之一**激活**端口：

* 订单设置中的 <mark style="color:purple;">**Restart proxy**</mark> 按钮
* 访问订单中的专属 **Reset URL** 链接

{% hint style="warning" %}
如果不使用代理，**3 小时**后端口将进入节能模式。该限制无法取消，要恢复运行只需再次调用 Restart proxy 或 Reset URL。
{% endhint %}

***

## 9. 移动代理是否提供无限流量？

是的，**移动代理流量无限制**。下载流量没有上限，仅按端口的租用周期计费。

***

## 10. 为什么我的移动代理 IP 会周期性变化？

移动代理位于我们的移动农场，通过真实的 SIM 卡运行。IP 地址的变化完全取决于**运营商**：

* 平均而言，运营商**每天**更新一次地址。
* 运营商可能在任何时刻启动池切换，地址会更早变化。

这是移动互联网的固有特性，**不在我们的控制范围内**。如果需要按计时器或热键进行轮换，请使用[我们扩展程序中的 IP Rotation](../../our-products/proxyshard-extension.md) 功能。

***

## 11. 住宅代理中的 TTL 和 Sticky 是什么？

* <mark style="color:purple;">**TTL**</mark>（Time-To-Live）- 会话的「生命周期」秒数。TTL 到期后，代理链路将被重建，您会获得新的 IP。取值范围为 60 至 86400 秒。
* <mark style="color:purple;">**Sticky / Random**</mark> - 会话模式。<mark style="color:purple;">Sticky</mark> 会尽量在 TTL 内保持相同的 IP，<mark style="color:purple;">Random</mark> 在每次新连接时分配随机 IP。

住宅代理订单所有参数的完整说明：[如何使用住宅代理](../../our-products/residential-proxies/how-to-use-residential-proxies.md)。

***

## 12. 住宅代理中的 Relay 参数是什么？

<mark style="color:purple;">**Relay**</mark> 是您的流量进入住宅设备池的**负载均衡（备用）服务器**。Relay 会根据**您连接的来源位置**进行选择，使路径更短、更稳定。

* 默认使用 <mark style="color:purple;">**EU**</mark>
* 同时可选 <mark style="color:purple;">**RU**</mark> 和 <mark style="color:purple;">**UA**</mark>

{% hint style="info" %}
Relay 的选择**不会影响**最终 IP 的国家/地区，它仅为负载均衡服务器。最终国家由订单设置中的 <mark style="color:purple;">Country</mark> 参数决定。
{% endhint %}

***

## 13. 住宅代理流量会在月底过期吗？

不会。未使用的流量不会在月底过期；它会一直保留，直到全部用完。如果流量耗尽，代理会暂时停止工作，只需点击订单右上角的 <mark style="color:purple;">**Add traffic**</mark>，补充流量包后，代理将立即恢复工作。

***

## 14. 为什么我的住宅代理 IP 会周期性变化？

住宅代理托管在真实用户的家庭设备上，这些用户参与了付费流量共享计划。这些设备可能会：

* 离开共享网络（例如设备被主人关闭），
* 出现信号 / 连接问题。

任何此类原因都会导致会话期间 IP 发生变化。我们不直接管理池中的设备。

{% hint style="info" %}
**如果会话工作异常或经常断开**，有两种方法可以更换地址：

**方法 1.** 点击订单中的 <mark style="color:purple;">**Generate proxy**</mark>，您将获得新的连接字符串。

**方法 2.** 在连接字符串中手动更改 <mark style="color:purple;">**SID**</mark>。例如，在如下字符串中：

```
relay-eu.proxyshard.com:8080:plan-limited-country-any-sid-8dbryym0a32i:7nnrpl63344545gx
```

登录名中包含 `sid-8dbryym0a32i` 片段。如果您将其中的一个字符更改为例如 `sid-8dbryym0a324`，IP 地址就会发生变化。点击 <mark style="color:purple;">Generate proxy</mark> 时，「底层」也是这样工作的。

<mark style="color:purple;">SID</mark> 负责为您的会话连接选择设备和 IP。
{% endhint %}

***

## 15. 为什么我经常收到 Google / Cloudflare 验证码？

Google 和 Cloudflare 验证码通常**不是由代理本身**造成的，而是由浏览器指纹造成的。最常见的原因：

* 使用了过时或低质量的反检测浏览器
* 配置文件指纹「黏滞」/ 重复
* 浏览器泄漏不一致的参数（timezone、language、WebRTC 等）

**怎么办：** 每次出现问题时重新生成配置文件指纹，使用优质反检测方案（例如 [Vision 浏览器](../../setup-guides/antidetect-browsers/vision-browser.md)），并通过 [IP Checker](../../our-products/ip-checker.md) 检测泄漏。

***

## 16. 你们的代理有哪些限制？

所有产品上均阻止：

* 经常被用于暴力破解攻击的服务端口：**22 (SSH)、23 (Telnet)、25 (SMTP)** 以及其他若干端口。
* 银行和政府机构的网站，以及 **Stripe** 和 **PayPal** 支付处理服务（这是监管要求）。

按端口、网站、按产品例外的完整限制列表，以及无限住宅代理的限制，请参阅[限制](../../our-products/restrictions.md)章节。

***

## 17. 支持哪些支付系统？

我们支持以下方式付款：

* <mark style="color:purple;">**Stripe**</mark> - 银行卡，最低付款金额 **$5**。
* <mark style="color:purple;">**Cryptomus**</mark> - 加密货币（BTC、LTC、USDT 等）。

{% hint style="info" %}
**关于通过 Cryptomus 的加密货币付款：**

* 通过 **BTC** 或 **LTC** 付款最长可能需要 **1 小时**处理，这取决于网络确认，而非我们的系统。
* 通过 **USDT** 付款需要最低金额 **$15**，且客户需承担手续费。这是 Cryptomus 平台自身的要求，我们对这些条款没有影响。
{% endhint %}

***

## 18. 你们有 API 吗？

是的，我们有完整的用户 API。

* **规范与 Try-it-out：** 本 GitBook 中的[用户 API](../../) 章节。
* **俄语使用示例：** [github.com/ProxyShard/proxyshard-api-examples-ru](https://github.com/ProxyShard/proxyshard-api-examples-ru)
* **英语使用示例：** [github.com/ProxyShard/proxyshard-api-examples](https://github.com/ProxyShard/proxyshard-api-examples)

***

## 19. 住宅代理可用哪些国家？

住宅代理覆盖**世界上大多数国家**。包含城市与地区的完整最新列表请参阅[可用国家列表](../../our-products/residential-proxies/available-countries.md)页面。

***

## 20. ISP 代理可用哪些国家？

截至 2026 年 6 月，ISP 代理在以下地区可用：

| 国家 |
| ---- |
| 🇨🇿 捷克 |
| 🇺🇸 美国（宾夕法尼亚州） |
| 🇹🇷 土耳其 |
| 🇺🇦 乌克兰 |

***

## 21. Datacenter 代理可用哪些国家？

截至 2026 年 6 月：

* 🇲🇩 摩尔多瓦
* 🇺🇦 乌克兰
* 🇳🇱 荷兰
* 🇩🇪 德国
* 🇵🇱 波兰
* 🇺🇸 美国（即将推出）

***

## 22. 移动代理可用哪些国家与运营商？

| 国家 | 运营商 |
| ---- | ------ |
| 🇺🇸 美国 | T-Mobile (5G)、Verizon (5G, 科罗拉多) |
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

该列表持续扩展。最新地区与价格可在 [Mobile proxy](https://dashboard.proxyshard.com/en/mobile-proxy) 购买页面查看。

***

## 23. 你们的价格是多少？

| 产品 | 价格 | 周期 / 单位 |
| ---- | ---- | ----------- |
| **ISP** | **$2** | 每个 IP / 月（+$0.6 用于 p0f） |
| **Residential** | **$2** | 每 GB |
| **Premium Residential** | **$3** | 每 GB |
| **Datacenter** | **$0.3 / $0.4 / $0.7 / $1.2** | 3 天 / 周 / 半月 / 月（+$0.3 用于 p0f，仅在租期一个月及以上时可用） |
| **Unlimited Residential** | **$30 / $199 / $399 / $699** | 天 / 周 / 半月 / 月 |
| **Mobile** | **$4 / 天起，$55 / 月** | 取决于国家和运营商 |

{% hint style="info" %}
每个套餐的确切价格和可用周期会直接显示在[控制面板](https://dashboard.proxyshard.com/)的购买页面。
{% endhint %}

***

## 24. 我需要 IPv4 连接，为什么连接字符串里是域名？

在 <mark style="color:purple;">**Mobile**</mark> 和 <mark style="color:purple;">**Residential**</mark> 代理上，默认的连接地址是一个**域名**，其背后隐藏着大量 IP 地址。域名后面是负载均衡（backconnect）服务器，再通过它们连接到代理设备，因此我们默认不在字符串中直接给出 IPv4。

连接字符串示例：

```
mobile.eu.proxyshard.com:1234:aabbbcc:password
resident.eu.proxyshard.com:8080:plan-limited-country-NL-sid-ABXdedq:AAAbbbbCC
```

如果您的软件必须使用 IPv4，可以**解析（resolve）**该域名，并用得到的地址替换域名。

**方法 1. 通过网站。** 打开 [www.nslookup.io](https://www.nslookup.io)，输入连接字符串中的域名，即可获得一组 IPv4 地址。例如，如果查询返回 `172.67.72.239`，那么就可以用这个 IP 替换 `mobile.eu.proxyshard.com`：

```
172.67.72.239:1234:aabbbcc:password
```

**方法 2. 在终端手动查询。** 在 Windows 或 Linux 中执行：

```
nslookup mobile.eu.proxyshard.com
```

响应中的 **Addresses** 部分会列出 IPv4 地址 - 任选其一替换域名即可。

{% hint style="warning" %}
域名后面有多台服务器，它们的 IP **可能发生变化**。如果用「写死的」IP 连接突然无法工作，请重新解析域名并替换为新地址。
{% endhint %}

***

## 25. 你们有 IPv6 吗？

没有，我们**仅出售 IPv4** 代理。

***

## 26. 移动代理上的轮换（更换 IP）是如何工作的？

除了运营商侧的自动地址更换（见问题 10）之外，您还可以**手动更换 IP，频率不超过每分钟一次**，方式有两种：

* 访问订单中的专属 <mark style="color:purple;">**Reset URL**</mark> 链接；
* 点击订单设置中的 <mark style="color:purple;">**Restart proxy**</mark> 按钮。

有关订单字段的更多信息，请参阅[移动代理](../../our-products/mobile-proxies.md)页面。

***

## 27. 代理上有通道消耗监控吗？

任何产品都不内置对所消耗通道**速度**的测量。可用的统计如下：

* <mark style="color:purple;">**Unlimited Residential**</mark> - 有活动连接计数器；
* <mark style="color:purple;">**Residential**</mark> - 有已用流量统计（以 GB 计）；
* 在**其他产品**（Datacenter、ISP、Mobile）上，**不进行**流量测量和请求日志记录。

***

## 28. 为什么 Standard 和 Unlimited 住宅代理使用 Cloudflare DNS？

这是因为目前在这些套餐上**已禁用对运营商服务器的 DNS 查询**，解析通过公共 DNS（Cloudflare）进行。

在 <mark style="color:purple;">**ISP**</mark> 和 <mark style="color:purple;">**Premium Residential**</mark> 代理上没有此限制。

***

## 29. 如何在代理上获得最低延迟（ping）？

在**住宅**和**移动**代理上，到终端节点的延迟取决于多个因素：

* 运营商基站的当前负载；
* 分发流量的设备上的信号质量；
* 您与接入点的距离。

此外，主要的负载均衡服务器位于**荷兰**。当连接到**美国**或**非洲**等地区时，除了您到均衡服务器的延迟外，还会叠加荷兰服务器与终端代理之间的额外延迟。无法缩短这条路径。

{% hint style="success" %}
如果对最低延迟和速度有要求，请使用 <mark style="color:purple;">**Datacenter**</mark> 或 <mark style="color:purple;">**ISP**</mark> 代理。它们的连接开销极低：没有负载均衡服务器这一层，连接是直连的。
{% endhint %}

为获得**尽可能低的 ping**，请从代理所在的同一国家进行连接。这通常通过在目标国家租用 <mark style="color:purple;">VPS / VDS / Bare-Metal</mark> 服务器来实现。例如，对于美国的 ISP 代理，理想做法是通过纽约的 VPS 工作 - ping 会最低，而从欧洲连接时 ping 至少为 **80–120 ms**。

***

## 30. 网站使用什么时区？

控制面板中的所有订单和日期均按 **UTC +0** 显示。

***

{% hint style="success" %}
没有找到您问题的答案？请联系我们的[支持](../../contact-us.md)，我们会尽快回复。
{% endhint %}
