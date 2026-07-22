---
icon: house-signal
---

# Standard Residential

<mark style="color:purple;">Standard Residential</mark> 是 ProxyShard 的基础住宅代理池。这些代理托管在通过标准筛选的真实家庭设备上。支持 <mark style="color:purple;">UDP</mark>，因此是 <mark style="color:purple;">WebRTC</mark> 相关任务的理想选择。

{% embed url="https://dashboard.proxyshard.com/en/residential-main" %}

## 特性

| 参数              | 值                              |
| --------------- | ------------------------------ |
| 池大小            | 300,000 - 400,000 台设备        |
| 最大连接数         | 35,000                         |
| 每个订单最大速度     | 75 Mbps                        |
| UDP 支持          | ✓（美国位置不可用）               |
| [Device OS 筛选 (p0f)](README.md#she-zhi-zi-duan-shuo-ming) | ✗ |
| 计费方式           | 按 GB（按量付费）                |
| 价格              | **$2 / GB**                    |

## 适用于哪些任务

- 自动化、抓取、机器人
- 配合反检测浏览器的多账户管理
- 需要 <mark style="color:purple;">UDP / WebRTC</mark> 支持的任务
- 处理屏蔽数据中心 IP 的平台

{% hint style="info" %}
需要去除流量限制？请参阅 [Unlimited Residential](unlimited-residential-proxy.md) - 同一个池，但不计 GB。\
需要最大且最干净的池？请参阅 [Premium Residential](premium-residential.md)。
{% endhint %}

您可以[在此处](../restrictions.md)查看产品限制。
