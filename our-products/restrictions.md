---
icon: hand
---

# 限制

此页面列出了我们产品的所有当前限制。

***

## 阻止特定网站

以下内容无法通过代理获得：

* 银行网站（网上银行、银行个人账户）
* 政府门户网站和网站
* 支付处理器：<mark style="color:purple;">Stripe</mark>、<mark style="color:purple;">PayPal</mark>（包括 <mark style="color:purple;">Yahoo</mark>）

这是旨在限制欺诈活动的监管要求。该块**不适用于**加密服务和支付系统，例如交易所。

{% hint style="warning" %}
适用于所有产品**除** [移动代理](mobile-proxies.md)。

Stripe 和 PayPal 可在数据中心和 ISP 代理上使用。
{% endhint %}

***

## 住宅代理上的 UDP（美国）

{% hint style="danger" %}
UDP 不适用于 **美国** 位置的 [住宅代理](residential-proxies/)（**包括无限**）:flag\_us:
{% endhint %}

这不是我们的限制。 2026 年初，美国提供商禁止未经网络内部事先启动的传入 UDP 连接。因此，代理上的 UDP 关联停止在此区域中工作。

UDP 在所有其他位置都可以正常工作。

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


