# ClashX

{% hint style="success" %}
该解决方案支持 UDP 隧道！
{% endhint %}

## **ClashX** 设置

转到 ClashX 项目的官方 GitHub 页面并下载适合您的操作系统所需的存档版本。该示例显示了 Windows 操作系统 ([Clash.for.Windows-0.20.39-win.7z](https://github.com/lantongxue/clash_for_windows_pkg/releases/download/0.20.39/Clash.for.Windows-0.20.39-win.7z)) 上的设置。

{% embed url="https://github.com/lantongxue/clash_for_windows_pkg/releases" %}

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

## **开始 ClashX**

然后解压压缩包并以_<mark style="color:red;">**管理员**</mark>_身份运行“Clash for Windows.exe”，如下例所示：

<figure><img src="../../.gitbook/assets/image (172).png" alt="" width="563"><figcaption><p>Unpacking the archive to the desktop</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (162).png" alt="" width="375"><figcaption><p>Run as administrator</p></figcaption></figure>

## **程序设置**

启动程序后，转到“<mark style="color:purple;">Profiles</mark>”并打开<mark style="color:purple;">config.yaml</mark>文件编辑器。

<figure><img src="../../.gitbook/assets/image (159).png" alt="" width="375"><figcaption></figcaption></figure>

## **配置文件设置**

按以下示例设置文件配置，并按顺序指定您的代理：

```yaml
proxies:
  - name: "ProxyShard-Germany-testname"
    type: socks5
    server: 123.123.123.123
    port: 1234
    username: proxy_login
    password: password_login
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

最后，它应该看起来大约像这样：

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="563"><figcaption><p>Configuration example</p></figcaption></figure>

{% hint style="info" %}
**您可以在[设置指南](../getting-started.md)部分找到代理设置示例**
{% endhint %}

<pre><code>代理：
- 名称：“ProxyShard-德国-测试名称”|这里设置代理名称
类型： 袜子5 |协议类型
服务器：123.123.123.123 |代理地址或域名
端口：1234 |代理端口
用户名： proxy_login |代理登录
密码：password_login |代理密码
UDP: 正确
代理组：
- 名称：“自动”
类型：选择
代理：
- ProxyShard-德国-测试名称

规则：
- 进程名称，<a data-footnote-ref href="#user-content-fn-1">chrome.exe</a>，自动|选择一个特定的应用程序进行代理
- 直接匹配 |在我们的示例中，使用 Chrome 浏览器，
|但它可以是任何应用程序，例如discord.exe
| - MATCH,DIRECT ：表示所有非 Chrome 的流量
|将不会路由到代理，而是路由到您的主界面
</code></pre>

## **检查配置**

配置完成后，打开“代理”，选择“全局”选项，然后检查您在步骤 4 中设置的配置。

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="563"><figcaption></figcaption></figure>

如果检查失败并显示“失败”，请比较配置文件并确保所有代理数据输入正确。如果设置正确，您将得到如下图所示的成功检查结果。

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

## **安装并启用 TAP 接口**

接下来，转到“常规”并在计算机上安装 TAP 界面。它将创建一个代理将绑定到的新接口。

安装TUN接口后，启用TUN模式，如截图第4帧所示。

<figure><img src="../../.gitbook/assets/image (163).png" alt="" width="563"><figcaption></figcaption></figure>

## **检查功能**

如果一切成功启动，请打开您配置的应用程序（步骤 4）并享受使用 UDP 流量代理的程序！<br>

在我们的示例中，Chrome 已被代理，我们可以使用 [checkers](../../our-products/about-udp/webrtc-leak-check-tools.md) 检查它。

<figure><img src="../../.gitbook/assets/image (164).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (165).png" alt="" width="563"><figcaption></figcaption></figure>

如果检查或代理[不起作用](../../faq-and-support/faq/proxy-not-working.md)，请确保您确实以管理员身份启动 ClashX 并正确完成步骤 4 到 6。

## **附加：添加多个代理并在它们之间切换**

要在代理之间快速切换，请将新代理添加到步骤 4 中的配置中。诸如“ProxyShard-DE-testname1”之类的名称是任意的，可以根据您的喜好进行设置。

添加它们后的关键点是还要在“proxy-group”中指定代理，如下所示：

```yaml
proxies:
  - name: "ProxyShard-DE-testname1"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true
    
  - name: "ProxyShard-NL-testname2"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

  - name: "ProxyShard-RO-testname3"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-DE-testname1
      - ProxyShard-NL-testname2
      - ProxyShard-RO-testname3

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

如果您正确指定了所有内容，其他连接点将出现在“代理”中。连接将根据所选的设置配置文件进行（只需单击其中任何一个）。

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

[^1]：代理申请



