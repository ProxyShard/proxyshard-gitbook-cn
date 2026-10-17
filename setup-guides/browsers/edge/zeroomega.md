---
description: 在 Microsoft Edge 中配置代理
---

# ZeroOmega

## 安装 ZeroOmega

{% hint style="warning" %}
ZeroOmega 仅支持 TCP 流量。如需使用 UDP，请改用 [Vision Browser](../../antidetect-browsers/vision-browser.md)。
{% endhint %}

从 Microsoft Edge Add-ons 安装 [ZeroOmega](https://microsoftedge.microsoft.com/addons/detail/proxy-switchyomega-3-zer/dmaldhchmoafliphkijbfhaomcgglmgd)。

{% embed url="https://microsoftedge.microsoft.com/addons/detail/proxy-switchyomega-3-zer/dmaldhchmoafliphkijbfhaomcgglmgd" %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-addons-get_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-addons-get_white.png" alt="在 Microsoft Edge 中安装 ZeroOmega">
  </picture>
</figure>

安装完成后，打开扩展程序菜单，将 ZeroOmega 固定到浏览器工具栏。

<figure><img src="../../../.gitbook/assets/edge-extensions-pin-zeroomega.png" alt="将 ZeroOmega 固定到 Microsoft Edge 工具栏"><figcaption></figcaption></figure>

## 配置 ZeroOmega

打开 ZeroOmega，然后选择 `Options`。

<figure><img src="../../../.gitbook/assets/edge-zeroomega-popup-options.png" alt="打开 ZeroOmega 设置"><figcaption></figcaption></figure>

在 `Profiles` 中点击 `New profile...`。

<div align="center"><figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-new-profile_white.png" alt="创建 ZeroOmega 配置文件">
  </picture>
</figure></div>

输入配置文件名称，选择 `Proxy Profile`，然后点击 `Create`。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-new-profile-dialog_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-new-profile-dialog_white.png" alt="设置 ZeroOmega 配置文件名称和类型">
  </picture>
</figure>

在配置文件设置中选择协议，并填写订单 `Proxy List` 中的服务器地址和端口。点击锁形图标即可添加用户名和密码。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-proxy-server_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-proxy-server_white.png" alt="在 ZeroOmega 中填写代理地址和端口">
  </picture>
</figure>

输入代理用户名和密码，然后确认更改。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-proxy-auth_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-proxy-auth_white.png" alt="在 ZeroOmega 中配置代理身份验证">
  </picture>
</figure>

{% hint style="info" %}
数据格式和订单示例请参阅[开始使用](../../getting-started.md)。
{% endhint %}

点击 `Apply changes` 保存配置文件。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-apply-changes_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-apply-changes_white.png" alt="保存 ZeroOmega 配置文件">
  </picture>
</figure>

从浏览器工具栏打开 ZeroOmega，然后选择刚才创建的配置文件。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-select-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-select-profile_white.png" alt="选择 ZeroOmega 配置文件">
  </picture>
</figure>

代理现已连接，可以在 Microsoft Edge 中使用。
