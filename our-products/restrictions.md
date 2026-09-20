---
icon: hand
---

# 限制

此页面列出了我们产品的所有当前限制。

***

## 阻止特定网站

以下内容无法通过代理获得：

* 银行网站（网上银行、银行个人账户）
* 政府门户网站和网站，以及 `.gov` 和 `.edu` 域名的网站
* 支付处理器：<mark style="color:purple;">Stripe</mark>、<mark style="color:purple;">PayPal</mark>（包括 <mark style="color:purple;">Yahoo</mark>）

这是旨在限制欺诈活动的监管要求。该块**不适用于**加密服务和支付系统，例如交易所。

{% hint style="warning" %}
适用于所有产品**除** [移动代理](mobile-proxies.md)。

Stripe 和 PayPal 可在数据中心和 ISP 代理上使用。
{% endhint %}

住宅代理的其他限制：

* [Standard Residential](residential-proxies/standard-residential.md) / [Unlimited Residential](residential-proxies/unlimited-residential-proxy.md) / [Premium Residential](residential-proxies/premium-residential.md) 无法使用 Microsoft 和 Apple 服务。

***

## 住宅代理上的 UDP

{% hint style="danger" %}
UDP 不适用于 **美国** 位置的 [Standard Residential](residential-proxies/standard-residential.md) 和 [Unlimited Residential](residential-proxies/unlimited-residential-proxy.md) :flag\_us:
{% endhint %}

这不是我们的限制。 2026 年初，美国提供商禁止未经网络内部事先启动的传入 UDP 连接。因此，代理上的 UDP 关联停止在此区域中工作。

Standard 和 Unlimited 在其他位置支持 UDP，但仍需遵守通用端口限制。

[Premium Residential](residential-proxies/premium-residential.md) 在所有位置支持 UDP，但部分城市及运行 macOS 或 iOS 的设备除外。

### Standard 和 Unlimited 的 UDP 端口限制

Standard 和 Unlimited 目前仅允许将 UDP 流量发送到目标端口 `8443`、`8080`、`3478` 和 `19302`，其他 UDP 端口范围均被阻止。美国位置仍然完全不支持 UDP。

Premium Residential 不受此端口限制影响，仅保留部分城市及 macOS/iOS 设备的现有例外情况。

Standard 和 Unlimited 的此项限制预计于 2026 年 10 月初解除。

### `static_mode2` 与 macOS/iOS 设备

`static_mode2` 对应 Premium Residential 的 `Session mode` 字段中的 `Static`。在此模式下，代理会保留选定的设备。当该设备暂时离线时，会话不会切换到其他设备。

如果选定的设备不可用，代理连接字符串可能会停止响应，直到设备重新上线或 `TTL` 到期。如需立即获取其他设备，请使用 `Generate proxy` 创建新的连接字符串。

使用 `Device OS: macOS` 或 `iOS` 筛选会显著缩小可用设备池。如果同时选择城市和运营商，可能找不到符合条件的设备，尤其是在 Tier 2 和 Tier 3 国家。部分 macOS/iOS 设备和某些城市也不支持 UDP。

***

## p0f 开启移动代理

设备指纹伪装 (p0f) 在某些国家/地区和运营商中不可用：

| 国家                       | 运营商           |
| -------------------------- | ---------------- |
| 英国 :flag\_gb:            | 所有运营商       |
| 爱尔兰 :flag\_ie:          | Vodafone         |
| 德国 :flag\_de:            | 所有运营商       |
| 荷兰 :flag\_nl:            | Vodafone         |
| 法国 :flag\_fr:            | 所有运营商       |
| 意大利 :flag\_it:          | Vodafone、WIND   |
| 波兰 :flag\_pl:            | Orange           |
| 印度尼西亚 :flag\_id:      | 所有运营商       |
| 新西兰 :flag\_nz:          | OneNZ            |
| 乌克兰 :flag\_ua:          | Life（Lifecell） |

在所有其他位置和运营商中，p0f 修改正常工作。

***

## 数据中心和 ISP 代理的连接数限制

[数据中心代理](datacenter-proxies.md)和 [ISP 代理](isp-proxies.md)的限制为：每个 IP 最多 **2,500 个连接**。

***

## 关闭端口

{% hint style="info" %}
适用于所有产品。 IMAP (993) 在 DC\ISP 代理上可用。
{% endhint %}

通过代理连接到经常用于攻击第三方服务的服务端口的连接被阻止：

|港口|协议|
| ---- | -------- |
| 21 | 21 FTP |
| 22 | 22 SSH |
| 23 | 23远程登录 |
| 25 | 25邮件发送 |

***

## 无限住宅代理的限制

* 基本连接数限制=5000。可以增加；更多详情请参见[支持](../contact-us.md)。
* 每个订单的最大速度 = 75 **Mbps**
