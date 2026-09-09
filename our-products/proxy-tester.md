---
icon: vial
---

# 代理测试器

<mark style="color:purple;">ProxyShard Proxy Tester</mark> 可直接在网站上快速检查代理是否可用，无需安装额外软件；使用 SOCKS5 时，还可以检查 UDP 支持。

{% embed url="https://proxyshard.com/proxy-tester" %}

***

<figure><img src="../.gitbook/assets/proxy-tester-check-result.png" alt=""><figcaption></figcaption></figure>

## 如何使用

1. 打开 [proxyshard.com/proxy-tester](https://proxyshard.com/proxy-tester)
2. 将一个或多个代理粘贴到 <mark style="color:purple;">**Proxy list**</mark> 字段中，每行一个
3. 点击 <mark style="color:purple;">**Test Proxy**</mark>
4. 等待下方 <mark style="color:purple;">**Proxy check history**</mark> 表格显示结果

***

## 特征

| 参数 | 值 |
| --------------------- | -------------------------------------------------------------------------------------- |
| **协议** | HTTP、SOCKS5 |
| **最大代理** |最多 100 |
| **限制** |每分钟 1 个请求 |
| **支持的格式** | `IP:PORT:LOGIN:PASSWORD`、`LOGIN:PASSWORD@IP:PORT`等标准格式|

***

## 结果显示什么

检查完成后，<mark style="color:purple;">**Proxy check history**</mark> 表格会显示：

| 字段 | 描述 |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Proxy** | 建立连接的 IP 地址 |
| **Response time** | 响应时间，以毫秒为单位。数值越低，代理速度越快 |
| **Status code** | HTTP 响应代码。`200` 表示连接正常 |
| **Result** | 最终状态为 <mark style="color:green;">**Success**</mark>（可用）或 <mark style="color:red;">**Failed**</mark>（不可用）。如果代理支持 UDP，状态旁会显示 <mark style="color:purple;">**UDP**</mark> 标记 |

***

## 如果代理检查失败

这并不总是意味着代理有故障。查看：

* 格式是否正确（登录名\密码\端口）
* 协议是否混淆(HTTP\SOCKS5)
* 购买后是否已过去2-3分钟（DC\ISP代理最多需要2分钟同步）
* 您的提供商是否有任何阻止

如果一切正确但检查仍然失败，请联系[支持](../contact-us.md)。

{% hint style="info" %}
如需更详细的诊断，您可以通过命令行检查代理。更多详情：[如何检查代理功能](../faq-and-support/faq/how-to-check-proxy.md)
{% endhint %}



