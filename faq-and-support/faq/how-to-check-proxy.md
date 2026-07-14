---
icon: flask-vial
---

# 如何检查代理是否工作

如果代理未连接，或者您想确保一切正常，可以使用两种简单的方法进行检查。

***

## 方法1：网站上的代理测试器

最快的选择。

打开我们的[代理测试器](https://proxyshard.com/proxy-tester)，将代理粘贴到字段中，然后单击“**测试代理**”。

请阅读[代理测试器](../../our-products/proxy-tester.md) 文章，了解有关功能和格式的更多信息。

***

## 方法2：通过curl（命令行）检查

当您需要直接从计算机快速检查连接时，此方法适用。它适用于 Windows、macOS 和 Linux。

### Windows

打开命令提示符：按 <mark style="color:blue;">WIN+R</mark>，输入 `cmd`，然后按 Enter。

### macOS / Linux

打开终端（在 macOS 上，通过 Spotlight 或应用程序 > 实用程序文件夹）。

***

### 检查 HTTP 代理

```bash
curl -x http://USERNAME:PASSWORD@PROXY_IP:PORT -I https://www.google.com
```

真实数据示例：

```bash
curl -x http://KWFFEKf:LDLFEPF@88.99.123.233:44454 -I https://www.google.com
```

### 检查 SOCKS5 代理

```bash
curl --socks5 USERNAME:PASSWORD@PROXY_IP:PORT -I https://www.google.com
```

例子：

```bash
curl --socks5 KWFFEKf:LDLFEPF@88.99.123.233:44454 -I https://www.google.com
```

***

### 如何解释结果

{% hint style="success" %}
**代理有效。** 如果响应包含 `HTTP/1.1 200 OK` 或 `HTTP/2 200`，则连接成功。
{% endhint %}

{% hint style="danger" %}
**代理不起作用。** 如果您收到 `Connection refused`、`Connection timed out` 或 `Could not resolve proxy` 等错误，则表明连接失败。
{% endhint %}

### 如果无法连接怎么办

1. 重新检查用户名、密码、IP 和端口。一个常见的错误是混淆了 **HTTP** 和 **SOCKS5** 端口
2. 尝试通过 VPN 连接，以排除 ISP 的阻止
3.购买后等待2-3分钟：服务器需要时间更新
4. 如果没有帮助，请联系[支持](../../contact-us.md)



