---
description: 安装 ShardBrowser、添加代理并启动第一个配置文件
icon: browser
---

# ShardBrowser

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-cover_black.svg" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-cover_white.svg" alt="ShardBrowser 标志">
  </picture>
</figure>

{% hint style="info" %}
ShardBrowser 是 ShardX 团队基于 Chromium 打造的反检测浏览器。每个配置文件都拥有真实设备的独立指纹（fingerprint）和独立代理，因此网站会把各个配置文件识别为不同的电脑。本程序免费提供，按原样交付。如遇严重问题，请在 [GitHub](https://github.com/ProxyShard/ShardBrowser/issues) 提交错误报告。
{% endhint %}

ShardBrowser 官方网站：[shardbrowser.com](https://shardbrowser.com/)。

<figure><img src="../.gitbook/assets/shardbrowser-website.png" alt="ShardBrowser 官方网站"><figcaption>ShardBrowser 官方网站</figcaption></figure>

## Windows 系统要求

| 组件       | 最低配置                               | 推荐配置                          |
| ---------- | -------------------------------------- | --------------------------------- |
| 操作系统   | Windows 10 22H2 或 Windows 11，64 位   | Windows 11 64 位                  |
| 架构       | x64 / x86\_64                          | x64                               |
| 处理器     | 双核 64 位，支持 SSE3                  | 四核及以上                        |
| 内存       | 4 GB                                   | 8 GB（大量配置文件时 16 GB）      |
| 磁盘空间   | 1 GB                                   | 5 GB 以上                         |
| 运行环境   | Microsoft Edge WebView2                | 最新版本                          |

---

## 在 Windows 上安装

下载最新版本：

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

在 <mark style="color:purple;">**Assets**</mark> 中选择安装程序 <mark style="color:purple;">`ShardBrowser.Launcher_<版本>_x64-setup.exe`</mark>。如果需要免安装版，请下载 <mark style="color:purple;">`ShardBrowser-Launcher-portable-win-x64.exe`</mark>。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-github-release-assets_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-github-release-assets_white.png" alt="在 Assets 中选择 x64-setup.exe">
  </picture>
  <figcaption>在 Assets 中选择 x64-setup.exe</figcaption>
</figure>

运行下载的文件。<mark style="color:purple;">Windows SmartScreen</mark> 可能会显示警告。点击 <mark style="color:purple;">**More info**</mark>，然后点击 <mark style="color:purple;">**Run anyway**</mark>。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-windows-smartscreen_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-windows-smartscreen_white.png" alt="SmartScreen：点击 Run anyway">
  </picture>
  <figcaption>SmartScreen：点击 Run anyway</figcaption>
</figure>

## 在 macOS 上安装

在 <mark style="color:purple;">**Assets**</mark> 中下载 <mark style="color:purple;">`ShardBrowser.Launcher_<版本>_aarch64.dmg`</mark>。此版本适用于配备 Apple Silicon 处理器的 Mac。

打开 `.dmg` 文件，将 <mark style="color:purple;">**ShardBrowser Launcher**</mark> 拖入 <mark style="color:purple;">**Applications**</mark>。由于此版本尚未经过公证，macOS 可能会阻止首次启动。请在 Terminal 中运行：

```bash
xattr -dr com.apple.quarantine "/Applications/ShardBrowser Launcher.app"
```

也可以前往 <mark style="color:purple;">**System Settings**</mark> → <mark style="color:purple;">**Privacy & Security**</mark> → <mark style="color:purple;">**Open Anyway**</mark> 允许应用运行。

## 在 Linux 上安装

<mark style="color:purple;">**Assets**</mark> 中提供 `.AppImage`、`.deb` 和 `.rpm` 安装包。运行 AppImage 前，请先授予执行权限：

```bash
chmod +x ShardBrowser.Launcher_<版本>_amd64.AppImage
./ShardBrowser.Launcher_<版本>_amd64.AppImage
```

使用以下命令安装 `.deb` 包：

```bash
sudo apt install ./ShardBrowser.Launcher_<版本>_amd64.deb
```

## 首次启动

安装并启动后会打开主界面 <mark style="color:purple;">**All profiles**</mark>。左侧是功能菜单：配置文件、代理、指纹、扩展、书签、自动化以及 ShardX 账户。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="ShardBrowser 主界面">
  </picture>
  <figcaption>ShardBrowser 主界面</figcaption>
</figure>

---

## 添加代理

进入 <mark style="color:purple;">**Proxies**</mark>，点击 <mark style="color:purple;">**+ Add proxies**</mark>。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-proxies-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-proxies-empty_white.png" alt="Proxies 页面">
  </picture>
  <figcaption>Proxies 页面</figcaption>
</figure>

在 <mark style="color:purple;">**Add proxies**</mark> 窗口中，在 <mark style="color:purple;">**Type for lines without one**</mark> 中选择类型（默认 <mark style="color:purple;">SOCKS5</mark>），然后每行粘贴一个代理。支持的格式：

```
host:port
host:port:user:pass
user:pass@host:port
socks5://user:pass@host:port
```

以 `#` 开头的行会被忽略。列表中已存在的代理（类型、主机、端口、用户名和密码均相同）会被跳过。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-paste_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-paste_white.png" alt="每行粘贴一个代理，然后点击 Preview">
  </picture>
  <figcaption>每行粘贴一个代理，然后点击 Preview</figcaption>
</figure>

点击 <mark style="color:purple;">**Preview**</mark>。在预览窗口中点击 <mark style="color:purple;">**Test all**</mark>，在添加前检测代理。检测完成后，每个代理都会显示状态和国家。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-preview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-preview_white.png" alt="点击 Test all，然后点击 Add 1 proxy">
  </picture>
  <figcaption>点击 Test all，然后点击 Add 1 proxy</figcaption>
</figure>

带有 <mark style="color:purple;">**UDP**</mark> 标记的代理支持 <mark style="color:purple;">SOCKS5 UDP</mark>，因此也支持 <mark style="color:purple;">WebRTC</mark>，这在应对严格的反欺诈系统时非常有用。如果没有 <mark style="color:purple;">**UDP**</mark> 标记，配置文件会切换到 <mark style="color:purple;">**TCP-only**</mark> 模式：IP 不会泄露，但流量在高级反欺诈系统看来可能可疑。我们强烈建议使用[支持 UDP 的代理](../our-products/about-udp/)。

<mark style="color:purple;">**Select working only**</mark> 只保留可用的代理处于选中状态。点击 <mark style="color:purple;">**Add 1 proxy**</mark>，代理就会出现在列表中。

---

## 创建第一个配置文件

进入 <mark style="color:purple;">**All profiles**</mark>，点击 <mark style="color:purple;">**+ New profile**</mark>。也可以通过 <mark style="color:purple;">**Import from clipboard**</mark> 从剪贴板导入配置文件。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-button_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-button_white.png" alt="All profiles 页面">
  </picture>
  <figcaption>All profiles 页面</figcaption>
</figure>

此时会打开 <mark style="color:purple;">**New profile**</mark> 窗口，包含 <mark style="color:purple;">**Basics**</mark>、<mark style="color:purple;">**Proxy**</mark>、<mark style="color:purple;">**Fingerprint**</mark> 和 <mark style="color:purple;">**Extensions**</mark> 选项卡。在 <mark style="color:purple;">**Basics**</mark> 中输入配置文件名称。这里还可以选择文件夹、标签、颜色，添加备注并载入 cookies 文件。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-basics_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-basics_white.png" alt="输入配置文件名称">
  </picture>
  <figcaption>输入配置文件名称</figcaption>
</figure>

在 <mark style="color:purple;">**Proxy**</mark> 选项卡中，从列表里选择已保存的代理。也可以通过 <mark style="color:purple;">**+ Add a new proxy**</mark> 直接添加新代理。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-proxy_white.png" alt="为配置文件选择代理">
  </picture>
  <figcaption>为配置文件选择代理</figcaption>
</figure>

<mark style="color:purple;">**Fingerprint**</mark> 选项卡中的参数无需修改，ShardBrowser 会根据所选系统自动匹配指纹。如有需要，可以选择<mark style="color:purple;">操作系统</mark>（macOS、Windows、Linux、Android）、具体指纹、显卡、CPU 核心数、内存、刷新率和屏幕分辨率。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-fingerprint_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-fingerprint_white.png" alt="配置文件的指纹设置">
  </picture>
  <figcaption>配置文件的指纹设置</figcaption>
</figure>

点击 <mark style="color:purple;">**Create profile**</mark>。

---

## 启动配置文件

配置文件会出现在列表中。右侧会打开配置文件卡片：代理、扩展、备注、指纹参数、时区和语言（默认根据代理确定）。点击 <mark style="color:purple;">**Start**</mark>。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-start_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-start_white.png" alt="点击 Start 启动配置文件">
  </picture>
  <figcaption>点击 Start 启动配置文件</figcaption>
</figure>

浏览器会以隔离的指纹和代理启动。起始页 `chrome://shardx` 列出了该配置文件的各项防护。

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-browser-started_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-browser-started_white.png" alt="配置文件已启动">
  </picture>
  <figcaption>配置文件已启动</figcaption>
</figure>

---

## 常见问题

### 应用无法启动

很可能没有安装 <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>。请下载并安装：

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

原版 Windows 10/11 镜像已自带 WebView2。精简版系统中可能已被移除。
