---
icon: octopus
---

# iOS 和 Android 版 Octo Browser

{% hint style="warning" %}
代理仅在已启动的 Octo Browser 配置文件内生效。设备上的其他应用仍使用常规互联网连接。
{% endhint %}

## 安装 Octo Browser

从 App Store 或 Google Play 下载 Octo Browser。

{% embed url="https://apps.apple.com/us/app/octo-browser/id6762627194" %}

{% embed url="https://play.google.com/store/apps/details?id=net.octobrowser.mobile&pli=1" %}

## 注册和登录

使用电子邮件创建账户，或点击 **Sign up with Apple**。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/octo-browser-ios-log-in_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/octo-browser-ios-log-in_white.png" alt="注册 Octo Browser 账户">
  </picture>
</figure>

注册完成后，使用相同的方式登录。

## 创建使用代理的配置文件

在 **Profiles** 页面点击 **Create Profile**。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/octo-browser-ios-create-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/octo-browser-ios-create-profile_white.png" alt="在 Octo Browser 中创建配置文件">
  </picture>
</figure>

在新配置文件的设置中点击 **Set a proxy**。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/octo-browser-ios-set-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/octo-browser-ios-set-proxy_white.png" alt="向 Octo Browser 配置文件添加代理">
  </picture>
</figure>

1. 在 **Type** 中选择 HTTP、HTTPS 或 SOCKS5。
2. 从相应的 ShardX 订单中复制完整连接字符串，并粘贴到 **Proxy** 字段。
3. 点击 **Check proxy**。检查成功后，应用会显示连接的 IP 地址、位置和时区。
4. 点击 **Done**。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/octo-browser-ios-proxy-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/octo-browser-ios-proxy-form_white.png" alt="在 Octo Browser 中检查代理">
  </picture>
</figure>

## 启动配置文件

点击 **Create & Start**，保存并立即启动配置文件。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/octo-browser-ios-profile-ready_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/octo-browser-ios-profile-ready_white.png" alt="启动使用代理的 Octo Browser 配置文件">
  </picture>
</figure>

设置完成。此 Octo Browser 配置文件的流量将通过所添加的代理传输。
