---
icon: book-open-lines
---

# 如何将住宅代理添加到应用程序

让我们回顾一下“<mark style="color:purple;">Proxy list</mark>”字段中的代理连接字符串代表什么。

有关将生成的代理添加到应用程序的分步示例，请参阅[设置指南](../../setup-guides/getting-started.md)。

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">**resident.proxyshard.com**</mark> - 这是代理连接 IP 地址。它以 DNS 名称的形式出现，因为该地址后面有许多 IPv4 地址（平衡器），并且 IPv4 地址可能会发生变化。

<mark style="color:purple;">**8080**</mark> - 连接端口。端口不影响IP地址轮换；它们仅更改为选择协议类型。

<mark style="color:purple;">**计划限制国家/地区任何sid-nd1fmhz1mfxy**</mark> - 登录。它之所以这么长，是因为它包含所选的国家、地区以及订单设置中指定的其他参数。登录还包含<mark style="color:purple;">**sid-sy06witplz6x**</mark>，负责IP。改变一个字符就会改变IP地址。

<mark style="color:purple;">**7g6d8jd1t7in**</mark> - 连接密码

{% hint style="info" %}
_创建代理列表时，代理不会按顺序保存。创建新代理时，旧代理不会停止工作。这意味着您可以随时根据需要创建任意数量的附加代理，而不会失去对旧代理的访问权限。_
{% endhint %}



