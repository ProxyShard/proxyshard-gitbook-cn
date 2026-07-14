---
description: 安装 ShardX Launcher、配置代理并启动第一个配置文件
icon: browser
---

# ShardX Launcher

{% hint style="info" %}
ShardX Launcher 以 MIT 许可证发布，是面向个人使用的免费工具。软件按「原样」提供。我们会定期发布更新，但不提供实时聊天支持——如遇严重问题，请在 [GitHub](https://github.com/ProxyShard/ShardBrowser/issues) 上提交 Bug 报告。
{% endhint %}

## 系统要求

### Windows

| 组件         | 最低要求                                          | 推荐配置                                            |
| ------------ | ------------------------------------------------- | --------------------------------------------------- |
| 操作系统     | Windows 10 22H2 或 Windows 11，64 位              | Windows 11 64 位                                    |
| 架构         | x64 / x86\_64                                     | x64                                                 |
| 处理器       | 双核 64 位，支持 SSE3                             | 四核及以上                                          |
| 内存         | 4 GB                                              | 8 GB（多配置文件并行运行建议 16 GB）                |
| 磁盘空间     | 1 GB                                              | 5 GB+                                               |
| 运行环境     | Microsoft Edge WebView2                           | —                                                   |

### macOS

| 组件     | 最低要求                        | 推荐配置             |
| -------- | ------------------------------- | -------------------- |
| 操作系统 | macOS 11 Big Sur 或更高版本     | 最新稳定版           |
| 处理器   | Apple Silicon M1 或更新         | Apple M2 或更新      |
| 内存     | 4 GB                            | 8 GB 及以上          |
| 磁盘空间 | 1 GB                            | 5 GB+                |

{% hint style="warning" %}
当前版本编译目标为 `aarch64-apple-darwin`，不支持搭载 Intel 处理器的 Mac。
{% endhint %}

---

## Windows 安装

下载最新版本：

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

在 <mark style="color:purple;">**Assets**</mark> 部分选择 <mark style="color:purple;">`.exe`</mark> 或 <mark style="color:purple;">`.msi`</mark> 文件。

<figure><img src="../.gitbook/assets/shardx-win-download.png" alt=""><figcaption>在 Assets 中选择 .exe 或 .msi</figcaption></figure>

运行下载的文件。<mark style="color:purple;">Windows SmartScreen</mark> 可能会弹出警告——点击 <mark style="color:purple;">**更多信息**</mark>，然后点击 <mark style="color:purple;">**仍然运行**</mark>。

<figure><img src="../.gitbook/assets/shardx-win-smartscreen.png" alt=""><figcaption>SmartScreen — 点击「Run anyway」</figcaption></figure>

安装程序将在几秒钟内完成。

<figure><img src="../.gitbook/assets/shardx-win-install-done.png" alt=""><figcaption>安装完成</figcaption></figure>

---

## macOS 安装

下载最新版本：

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

在 <mark style="color:purple;">**Assets**</mark> 部分选择 <mark style="color:purple;">`aarch64.dmg`</mark> 文件。

<figure><img src="../.gitbook/assets/shardx-mac-download.png" alt=""><figcaption>在 Assets 中选择 aarch64.dmg</figcaption></figure>

打开下载的 `.dmg`，将 <mark style="color:purple;">**ShardX Launcher**</mark> 拖入 <mark style="color:purple;">**应用程序（Applications）**</mark> 文件夹。

<figure><img src="../.gitbook/assets/shardx-mac-install-dmg.png" alt=""><figcaption>将图标拖入 Applications 文件夹</figcaption></figure>

### 解除 Gatekeeper 限制

{% hint style="warning" %}
此步骤为必要操作。macOS 会阻止所有未经签名的应用——跳过此步骤将无法打开程序。
{% endhint %}

通过以下两种方式之一打开 <mark style="color:purple;">**终端（Terminal）**</mark>：

- <mark style="color:purple;">**Spotlight：**</mark> 按 `⌘ + 空格`，输入 `terminal`，选择应用

<figure><img src="../.gitbook/assets/shardx-mac-find-terminal.png" alt=""><figcaption>通过 Spotlight 查找终端</figcaption></figure>

- <mark style="color:purple;">**Finder：**</mark> 应用程序（Applications）-> 实用工具（Utilities）-> 终端（Terminal）

粘贴以下命令并按 <mark style="color:purple;">**Enter：**</mark>

```bash
xattr -dr com.apple.quarantine "/Applications/ShardX Launcher.app"
```

<figure><img src="../.gitbook/assets/shardx-mac-xattr-command.png" alt=""><figcaption>命令执行时无任何输出——这是正常的</figcaption></figure>

完成后，通过 <mark style="color:purple;">Spotlight</mark>（`⌘ + 空格` → `shardx`）或从 <mark style="color:purple;">应用程序（Applications）</mark> 文件夹启动应用。

<figure><img src="../.gitbook/assets/shardx-mac-open-spotlight.png" alt=""><figcaption>通过 Spotlight 启动 ShardX</figcaption></figure>

---

## 首次启动

首次启动时，ShardX 将从 CDN 下载浏览器引擎（约 198 MB，仅需一次）。请等待下载完成。

<figure><img src="../.gitbook/assets/shardx-win-first-run.png" alt=""><figcaption>首次启动时下载引擎</figcaption></figure>

下载完成后，将打开主界面 <mark style="color:purple;">**Browsers**</mark>。

<figure><img src="../.gitbook/assets/shardx-win-ready.png" alt=""><figcaption>ShardX Launcher 主界面</figcaption></figure>

---

## 添加代理

进入 <mark style="color:purple;">**Proxies**</mark> 部分，点击 <mark style="color:purple;">**+ New proxy**</mark>。

<figure><img src="../.gitbook/assets/shardx-setup-proxy-empty.png" alt=""><figcaption>Proxies 部分</figcaption></figure>

在 <mark style="color:purple;">**Bulk import proxies**</mark> 窗口中，每行粘贴一条代理。支持的格式：

```
host:port
host:port:user:pass
scheme://host:port
scheme://user:pass@host:port
```

<figure><img src="../.gitbook/assets/shardx-setup-add-proxy.png" alt=""><figcaption>每行粘贴一条代理</figcaption></figure>

点击 <mark style="color:purple;">**Test all**</mark>，在导入前检测代理可用性。

<figure><img src="../.gitbook/assets/shardx-setup-check-proxy.png" alt=""><figcaption>点击「Test all」检测，然后点击「Import」</figcaption></figure>

检测完成后，每条代理将显示状态。带有 <mark style="color:purple;">**UDP**</mark> 标记的代理支持 <mark style="color:purple;">SOCKS5 UDP</mark>，同时也支持 <mark style="color:purple;">WebRTC</mark>——这在对抗严格反欺诈系统时非常有用。如果没有 <mark style="color:purple;">**UDP**</mark> 标记，浏览器配置文件将自动切换为 <mark style="color:purple;">**TCP-only**</mark> 模式：IP 不会泄露，但流量可能会被高级反欺诈系统判定为可疑。我们强烈建议使用[支持 UDP 的代理](../our-products/about-udp/)。

点击 <mark style="color:purple;">**Import**</mark>——代理将出现在列表中，状态为 <mark style="color:purple;">**Active**</mark>。

<figure><img src="../.gitbook/assets/shardx-setup-proxy-done.png" alt=""><figcaption>代理已添加</figcaption></figure>

---

## 创建第一个配置文件

进入 <mark style="color:purple;">**Browsers**</mark> 部分，点击 <mark style="color:purple;">**+ New profile**</mark>。

<figure><img src="../.gitbook/assets/shardx-setup-profiles-empty.png" alt=""><figcaption>Browsers 部分</figcaption></figure>

无需更改默认参数——ShardX 会自动生成唯一的<mark style="color:purple;">浏览器指纹（fingerprint）</mark>。请务必在表单底部的 <mark style="color:purple;">**Proxy**</mark> 字段中选择代理。

<figure><img src="../.gitbook/assets/shardx-setup-new-profile.png" alt=""><figcaption>选择代理并点击「Create profile」</figcaption></figure>

点击 <mark style="color:purple;">**Create profile**</mark>。

<figure><img src="../.gitbook/assets/shardx-setup-profile-proxy-check.png" alt=""><figcaption>配置文件已创建</figcaption></figure>

---

## 启动配置文件

点击 <mark style="color:purple;">**Start**</mark>——浏览器将以独立指纹和代理启动。

<figure><img src="../.gitbook/assets/shardx-setup-done.png" alt=""><figcaption>配置文件已启动</figcaption></figure>

---

## 常见问题

### Windows：程序无法启动

很可能是未安装 <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>。请下载并安装：

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

原版 Windows 10/11 已内置 WebView2。精简版系统中可能已被删除。

### macOS：「ShardX Launcher 已损坏，无法打开」

这是 <mark style="color:purple;">Gatekeeper</mark> 的标准拦截行为。请按照[解除 Gatekeeper 限制](#jie-chu-gatekeeper-xian-zhi)部分的步骤操作——其中包含打开终端的两种方式以及解除隔离的命令。

---

## 下一步

- **自动化：** 通过 `127.0.0.1:40325` 上的[本地 HTTP API](../our-products/shardx-launcher.md) 管理配置文件
- **MCP 服务器：** 从设置中下载（<mark style="color:purple;">Settings -> MCP server</mark>）以通过 AI 代理控制配置文件
