# 代理链

## 代理链（Proxychains4）设置

从存储库安装 proxychains4 包

```bash
apt install proxychains4
```

## **配置设置**

打开 <mark style="color:$info;">**/etc/proxychains4.conf**</mark> 中的配置，并在其中指定协议和代理连接详细信息。

<figure><img src="../../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**您可以在[设置指南](../../getting-started.md)部分找到代理设置示例**
{% endhint %}

## **检查操作**

指定连接设置后，您可以通过向 ifconfig.me 发送请求来检查功能。

```
proxychains curl ifconfig.me
```

**如果检查确认您的 IP 地址已更改，您现在可以开始使用代理！**



