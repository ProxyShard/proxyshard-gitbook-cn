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

## 套餐

| 参数              | [Standard](standard-residential.md) | [Unlimited](unlimited-residential-proxy.md) | [Premium](premium-residential.md) |
| --------------- | ------------------------------------ | ------------------------------------------- | --------------------------------- |
| 池大小            | 300k - 400k                          | 300k - 400k (= Standard)                    | 3.8M - 4.6M                       |
| 最大连接数         | 35,000                               | 5,000                                       | -                                 |
| 最大速度           | 75 Mbps                              | 75 Mbps                                     | 75 Mbps                           |
| [UDP 支持](../about-udp/) | ✓（美国除外）                          | ✓（美国除外）                                | ✗                                 |
| [Device OS 筛选 (p0f)](README.md#she-zhi-zi-duan-shuo-ming) | ✗ | ✗ | ✓ |
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

## **如何开始使用它们？**

住宅代理的费用是根据订单购买的千兆字节数计算的。要访问国家/地区选择和其他参数，您需要[**购买**](https://dashboard.proxyshard.com/en/residential-main)订单。为此，请转到页面 ![](<../../.gitbook/assets/image (70).png>) 并指定千兆字节数。<br>

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

## 设置字段说明

在订单中，您可以找到几个重要的项目和选项。让我们回顾一下它们。

<figure><img src="../../.gitbook/assets/residential-proxy-settings.png" alt="包含 Device OS 和 Session mode 参数的 Residential Proxy 设置"><figcaption></figcaption></figure>

<mark style="color:purple;">**已使用流量**</mark> - 已使用多少\已购买多少

<mark style="color:purple;">**国家**</mark> - 国家/地区选择

<mark style="color:purple;">**地区**</mark> - 国家/地区选择

<mark style="color:purple;">**城市**</mark> - 区域城市选择

<mark style="color:purple;">**ISP**</mark> - 服务商类型选择。仅适用于 [Premium Residential](premium-residential.md)。

[**Device OS**](../p0f-spoofing.md) - 按设备操作系统筛选 [Premium Residential](premium-residential.md) 池。选择所需的操作系统，即可获取来自对应操作系统设备的代理。仅适用于 Premium Residential。

{% hint style="warning" %}
此设置会显著减少可用设备池。建议仅在定位人口超过 100 万的城市，或使用国家/地区级定位时启用。
{% endhint %}

<mark style="color:purple;">**会话**</mark> - 会话类型选择。可用选项有 <mark style="color:purple;">Sticky</mark> 和 <mark style="color:purple;">Rotate</mark>。

* <mark style="color:purple;">Sticky</mark> 允许您保留一个 IP 地址，具体取决于所选的 TTL 参数。
* <mark style="color:purple;">Rotate</mark> 在每次请求时都会更改 IP。 <mark style="color:purple;">Sticky</mark> 的 IP 范围池小于 <mark style="color:purple;">Rotate</mark> 的 IP 范围池。

<mark style="color:purple;">**Session mode**</mark> - 会话管理参数，仅适用于 [Premium Residential](premium-residential.md)。

* <mark style="color:purple;">Default (5 sec)</mark>：设备超过 5 秒未响应时切换会话。
* <mark style="color:purple;">Static</mark>：不会切换会话，并会在 TTL 指定的时间内等待设备重新接入网络。如果未设置 TTL，会话将固定一天。

<mark style="color:purple;">**协议**</mark> - HTTP/SOCKS。这些是连接代理服务器的主要协议。

<mark style="color:purple;">**TTL**</mark> - 选择 <mark style="color:purple;">Session - Sticky</mark> 时出现，并控制 IP 地址生命周期 (<mark style="color:purple;"> 生存时间 </mark>)。 <mark style="color:purple;">TTL</mark> 的最短时间为 60 秒（1 分钟）。

<mark style="color:purple;">**继电器**</mark> **-** 仅在存在连接问题时设置。

<mark style="color:purple;">**用户名\密码\主机\端口**</mark> - 连接数据。它还在代理列表中生成并支持条件格式。

{% hint style="info" %}
代理端口不会影响您收到的最终地址。它们只是远程代理服务器的端口号，仅此而已！
{% endhint %}

<mark style="color:purple;">**流量统计**</mark> - 每分钟使用流量统计。显示可能会延迟 10-20 分钟。

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

在订单末尾，您可以找到住宅流量的请求统计信息。在极少数情况下，可能会出现长达 20 分钟的显示延迟。

## **设置指南**

1. 指定设置：<mark style="color:purple;">Country</mark>、<mark style="color:purple;">Region</mark> 以及其他参数（如果需要）。

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. <mark style="color:purple;">HTTP</mark> 或 <mark style="color:purple;">SOCKS5</mark> 协议由您自行设置 <mark style="color:$info;">（一般情况下，SOCKS5 用于 UDP）</mark>。

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

3. 仅当存在连接问题时才指定服务器 (<mark style="color:purple;">Relay</mark>)。

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. 根据需要设置其他参数。

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

5. 单击 <img src="../../.gitbook/assets/image (76).png" alt="" data-size="line"> 按钮并从 <mark style="color:purple;"> 代理列表 </mark> 复制代理。

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

稍后，如果您需要其他国家/地区，请指定新设置，单击 <img src="../../.gitbook/assets/image (76).png" alt="" data-size="line">，然后在建立连接的应用程序中重新安装新代理。

{% hint style="info" %}
有关连接格式的更多信息，请访问此[链接](how-to-use-residential-proxies.md)。
{% endhint %}

{% hint style="warning" %}
“代理列表”中的代理不会保存，因为这是一个动态字段。您可以为不同位置生成许多代理：生成新代理时旧代理不会停止工作。
{% endhint %}

## 适用于哪些任务

社交网络与多账户管理、加密货币交易所（Binance、Bybit 等）、Polymarket、网页抓取、SEO 监控、广告验证（ad verification）、电商分析、价格监控、地理定向网站测试。

## 住宅代理的优缺点

#### <mark style="color:green;">优点：</mark>

* **灵活计费** - 按量付费或无限订阅（Unlimited）
* **更换 IP** - 按需或按计时器（TTL）轮换地址
* **广泛的地理定位** - 可选择国家、地区、城市和运营商
* **家庭来源地址** - IP 注册在家庭宽带运营商名下
* **UDP 支持** - Standard 和 Unlimited 可用（美国位置除外）

#### <mark style="color:red;">缺点：</mark>

* **可能出现速度下降** - 取决于终端设备的网络质量，这是该产品的特性
* **动态 IP** - 地址可能随时被切换；如需静态 IP，请参阅 [ISP](../isp-proxies.md) 或 [Datacenter](../datacenter-proxies.md)
* **不支持 p0f 伪装** - Premium Residential 仅提供 [Device OS 筛选](README.md#she-zhi-zi-duan-shuo-ming)
* **美国位置不支持 UDP** - 在 Standard 和 Unlimited 上

{% hint style="success" %}
没有 UDP 或需要静态地址？[ISP 代理](../isp-proxies.md)同时满足这两点。
{% endhint %}

{% hint style="info" %}
您可以在我们的[设置指南](../../setup-guides/getting-started.md)部分了解如何配置代理。
{% endhint %}
