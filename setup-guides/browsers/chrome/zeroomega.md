---
description: 在 Chrome 中配置代理
---

# ZeroOmega

## 安装 ZeroOmega

{% hint style="warning" %}
ZeroOmega 仅支持 TCP 流量。如需使用 UDP，请改用 [Vision Browser](../../antidetect-browsers/vision-browser.md)。
{% endhint %}

从 Chrome Web Store 安装 [ZeroOmega](https://chromewebstore.google.com/detail/pfnededegaaopdmhkdmcofjmoldfiped)。

{% embed url="https://chromewebstore.google.com/detail/pfnededegaaopdmhkdmcofjmoldfiped" %}

安装完成后，打开扩展程序菜单，将 ZeroOmega 固定到浏览器工具栏。

<figure><img src="../../../.gitbook/assets/chrome-extensions-pin-zeroomega.png" alt="将 ZeroOmega 固定到 Chrome 工具栏"><figcaption></figcaption></figure>

打开 ZeroOmega，然后选择 `Параметры`。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-open-options_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-open-options_white.png" alt="打开 ZeroOmega 设置">
  </picture>
</figure>

## 配置代理

在配置文件区域点击 `Новый профиль...`。

<div align="center"><figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-new-profile_white.png" alt="创建 ZeroOmega 配置文件">
  </picture>
</figure></div>

输入配置文件名称，选择 `Профиль прокси`，然后点击 `Создать`。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-new-profile-dialog_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-new-profile-dialog_white.png" alt="设置 ZeroOmega 配置文件名称和类型">
  </picture>
</figure>

在配置文件设置中选择协议，并填写订单 `Proxy List` 中的服务器地址和端口。点击锁形图标即可添加用户名和密码。

{% hint style="info" %}
数据格式和订单示例请参阅[开始使用](../../getting-started.md)。
{% endhint %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-proxy-server_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-proxy-server_white.png" alt="在 ZeroOmega 中填写代理地址和端口">
  </picture>
</figure>

输入代理用户名和密码，然后点击 `Сохранить изменения`。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-proxy-auth_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-proxy-auth_white.png" alt="在 ZeroOmega 中配置代理身份验证">
  </picture>
</figure>

点击 `Применить изменения` 保存配置文件。

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-apply-changes_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-apply-changes_white.png" alt="保存 ZeroOmega 配置文件">
  </picture>
</figure>

从浏览器工具栏打开 ZeroOmega，然后选择刚才创建的配置文件。

<figure><img src="../../../.gitbook/assets/chrome-zeroomega-select-profile.png" alt="选择 ZeroOmega 配置文件"><figcaption></figcaption></figure>

代理现已连接，可以在 Chrome 中使用。
