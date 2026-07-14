---
icon: arrows-rotate
---

# 为什么住宅代理没有保存

{% hint style="info" %}
这是正常行为。住宅代理是动态的，将生成的会话存储在代理列表中根本没有意义。
{% endhint %}

## 为什么会这样

住宅代理与 [数据中心](../../our-products/datacenter-proxies.md) 和 [ISP](../../our-products/isp-proxies.md) 代理不同，因为代理 IP 地址托管在真实的住宅设备上。

每一代都会创建一个具有唯一标识符的新会话，并临时绑定一个 IP。这就是列表不保存的原因：轮换后它会立即过时。

## 旧会话不会消失

{% hint style="success" %}
当您生成具有不同设置的新代理时，**旧代理将继续工作**并且不会更改其参数。每个会话都独立于其他会话而存在。
{% endhint %}

### 例子

假设您生成了德国代理：

```
relay-eu.proxyshard.com:8080:plan-limited-country-de-sid-aaaaaaaaa:xxxxxxxxx
```

让我们分解一下连接字符串：

| 部分 | 值 |
| ------------------------- | ---------------------------------------------------------------------------------- |
| `relay-eu.proxyshard.com` |负载均衡服务器（中继）|
| `8080` |服务器端口 |
| `plan-limited` |代理关税（`limited` - 常规，`unlimited` - 无限制，`premium` - 高级）|
| `country-de` |连接国家： 德国 (`de`) |
| `sid-aaaaaaaaa` | IP地址绑定的唯一会话ID |
| `xxxxxxxxx`               |连接密码|

例如，如果之后您生成美国代理，则会出现一个带有 `country-us` 和另一个 `sid` 的新字符串。但德国会话 `sid-aaaaaaaaa` **不会去任何地方**，并将继续使用相同的 IP 工作，直到会话过期。

{% hint style="warning" %}
如果您需要永久IP，请使用[数据中心](../../our-products/datacenter-proxies.md)或[ISP代理](../../our-products/isp-proxies.md)\
这些部分的代理具有静态 IP，并且仅颁发给一个用户
{% endhint %}
