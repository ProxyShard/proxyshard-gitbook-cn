---
description: 支持 UDP 代理的反检测浏览器
---

# Vision Browser

{% hint style="success" %}
Vision Browser 支持通过 SOCKS5 代理传输 TCP 和 UDP 流量。
{% endhint %}

## 安装和注册

打开 [Vision Browser 网站](https://browser.vision/r/ecf2408f-02de-4e4f-bc24-be368ac32325)，下载并安装应用。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-website-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-website-download_white.png" alt="下载 Vision Browser">
  </picture>
</figure>

创建账号。登录应用时需要使用这些信息。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-sign-up_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-sign-up_white.png" alt="注册 Vision Browser 账号">
  </picture>
</figure>

购买套餐时，可使用优惠码 `PROXYSHARD` 享受 20% 折扣。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-plan-promo-code_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-plan-promo-code_white.png" alt="Vision Browser 中的 PROXYSHARD 优惠码">
  </picture>
</figure>

## 创建第一个配置

1. 打开 `Profiles`。
2. 进入 `Folders`，点击 `Create folder`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folders-create_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folders-create_white.png" alt="在 Vision Browser 中创建配置文件夹">
  </picture>
</figure>

输入文件夹名称并保存。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folder-create-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folder-create-form_white.png" alt="设置配置文件夹名称">
  </picture>
</figure>

在新文件夹中点击 `Create profile`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-profiles-create-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-profiles-create-profile_white.png" alt="创建 Vision Browser 配置">
  </picture>
</figure>

在 ShardX 面板中生成一个 SOCKS5 代理，并复制连接信息。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-single_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-single_white.png" alt="在 ShardX 中生成一个 SOCKS5 代理">
  </picture>
</figure>

在 Vision 配置设置中打开 `SOCKS` 选项卡，填写代理信息，检测连接，然后点击 `Save`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-create-profile-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-create-profile-socks_white.png" alt="Vision 配置中的 SOCKS5 代理设置">
  </picture>
</figure>

<figure><img src="../../.gitbook/assets/vision-folder-profile-created.png" alt="已创建的 Vision Browser 配置"><figcaption></figcaption></figure>

## 添加代理列表

打开 `Proxies` 选项卡，点击 `Add proxy`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-add-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-add-proxy_white.png" alt="在 Vision Browser 中添加代理">
  </picture>
</figure>

在 ShardX 面板中生成 SOCKS5 代理列表并复制。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-list_white.png" alt="生成 SOCKS5 代理列表">
  </picture>
</figure>

将列表粘贴到添加字段中。导入后，请确认各连接显示 `Online`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-imported-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-imported-list_white.png" alt="Vision Browser 中已导入的代理">
  </picture>
</figure>

要为现有配置分配代理，请点击 `Proxy` 列中的图标。

<figure><img src="../../.gitbook/assets/vision-profiles-proxy-column.png" alt="配置列表中的 Proxy 列"><figcaption></figcaption></figure>

选择 `Select proxy`，指定连接并执行检测。

<figure><img src="../../.gitbook/assets/vision-edit-profile-select-proxy.png" alt="为 Vision 配置选择代理"><figcaption></figcaption></figure>

保存后，代理会显示在配置所在行。

<figure><img src="../../.gitbook/assets/vision-profile-proxy-assigned.png" alt="代理已分配给 Vision 配置"><figcaption></figcaption></figure>

## 检查 WebRTC

启动配置并打开 [ShardX IP Checker](https://proxyshard.com/ip-checker)。TCP 和 WebRTC 地址应保持一致。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-webrtc-check_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-webrtc-check_white.png" alt="检查 Vision Browser 的 TCP 和 WebRTC 地址">
  </picture>
</figure>
