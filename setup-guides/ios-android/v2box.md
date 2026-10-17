# V2Box

{% hint style="success" %}
V2Box 支持 UDP 流量。
{% endhint %}

## 安装 V2Box

从设备对应的应用商店安装 V2Box。

#### <mark style="color:green;">Android</mark>

{% embed url="https://play.google.com/store/apps/details?id=dev.hexasoftware.v2box" %}

#### <mark style="color:blue;">**iOS**</mark>

{% embed url="https://apps.apple.com/app/v2box-v2ray-client/id6446814690" %}

## 配置 V2Box

1. 打开 `Configs`。
2. 点击 `+` 创建配置。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-configs-add_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-configs-add_white.png" alt="在 V2Box 中添加配置">
  </picture>
</figure>

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-add-manual-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-add-manual-config_white.png" alt="在 V2Box 中手动配置">
  </picture>
</figure>

在 `Protocol` 中选择 `SOCKS`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-protocol-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-protocol-socks_white.png" alt="在 V2Box 中选择 SOCKS 协议">
  </picture>
</figure>

在 `Remarks` 中输入配置名称。使用订单 `Proxy List` 中的数据填写 `Address`、`Port`、`Username` 和 `ID/Password/Key`，然后点击 `Save`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-server-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-server-form_white.png" alt="在 V2Box 中配置代理">
  </picture>
</figure>

{% hint style="info" %}
数据格式和订单示例请参阅[开始使用](../getting-started.md)。
{% endhint %}

返回 `Configs`，选择刚才创建的配置，然后使用 `Slide to Connect` 建立连接。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-connected_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-connected_white.png" alt="在 V2Box 中连接代理">
  </picture>
</figure>

使用 [Proxy Tester](../../our-products/proxy-tester.md) 检查连接。
