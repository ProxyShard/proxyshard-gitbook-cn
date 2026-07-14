# v2rayN 图形用户界面

{% hint style="success" %}
该解决方案支持 UDP 隧道！
{% endhint %}

## v2rayN 设置。

点击[链接](https://github.com/2dust/v2rayN/releases)下载V2rayN。

{% embed url="https://github.com/2dust/v2rayN/releases" %}

<figure><img src="../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

或者通过控制台下载包。

```bash
wget https://github.com/2dust/v2rayN/releases/download/7.14.12/v2rayN-linux-64.deb
```



## **安装和启动**

通过“<mark style="color:purple;">Discover</mark>”安装下载的包或者通过命令行安装。

<figure><img src="../../../.gitbook/assets/Image00001 (11).PNG" alt=""><figcaption></figcaption></figure>

```bash
apt install ./v2rayN-linux-64.deb
```

然后通过“<mark style="color:purple;">Start</mark>”或命令行启动应用程序。

<figure><img src="../../../.gitbook/assets/Image00002 (12).PNG" alt=""><figcaption></figcaption></figure>

{% code fullWidth="false" %}
```
v2ray
```
{% endcode %}

## **配置文件设置**

创建新配置并指定 SOCKS / HTTP 作为连接协议。

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**您可以在[设置指南](../../getting-started.md)部分找到代理设置示例**
{% endhint %}

## **连接配置文件设置**

将从订单复制的代理粘贴到相应字段中，确保指定配置核心（<mark style="color:purple;">Xray</mark> 或 <mark style="color:purple;">SingBox</mark>），然后保存设置。

<figure><img src="../../../.gitbook/assets/Image00003 (6).PNG" alt=""><figcaption></figcaption></figure>

## 启动客户端

通过启用 <mark style="color:purple;">Tun</mark> 模式来启动客户端。

<figure><img src="../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

**完毕！您现在可以通过隧道传输所有流量来充分使用代理。**
