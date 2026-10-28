---
icon: triple-chevrons-up
---

# Unlimited Residential

<mark style="color:purple;">Unlimited Residential</mark> 基于 [Standard Residential](standard-residential.md) 池 - 相同的设备、相同的国家、相同的 IP 范围。主要区别在于：**没有流量限制**。当按 GB 计费的 Standard 变得昂贵时，该套餐更具优势。

{% embed url="https://dashboard.shardx.com/en/residential-unlimited" %}

购买和付款的分步说明：[购买住宅代理](../../site-navigation/buying-and-renewing/buying-residential-proxies.md)。

## 特性

| 参数              | 值                                          |
| --------------- | ------------------------------------------- |
| 池大小            | 300,000 - 400,000 台设备（= Standard）       |
| 最大连接数         | 5,000                                       |
| 每个订单最大速度     | 75 Mbps                                     |
| [UDP 支持](../about-udp/) | 支持（美国除外；受[端口限制](../restrictions.md)） |
| [Device OS 筛选](../p0f-spoofing.md) | 不支持 |
| 计费方式           | 日 / 半月 / 月                               |
| 价格              | **$30** / 天 · **$199** / 周 · **$399** / 半月 · **$699** / 月 |

{% hint style="warning" %}
Unlimited 套餐最多支持 5,000 个并发连接。该限制涵盖 `ESTAB`、`FIN_WAIT` 等所有连接状态，目前无法提高。专属套餐仍在开发中，暂未开放。
{% endhint %}

## 适用于哪些任务

- 高流量消耗的自动化
- 不想计较 GB 的长期流程
- 需要 <mark style="color:purple;">UDP / WebRTC</mark> 支持的任务

{% hint style="info" %}
想按 GB 付费而不是订阅？请参阅 [Standard Residential](standard-residential.md)。\
需要更大且支持精细定位的池？请参阅 [Premium Residential](premium-residential.md)。
{% endhint %}

您可以[在此处](../restrictions.md)查看产品限制。
