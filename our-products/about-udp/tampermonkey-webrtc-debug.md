---
description: 在 Chrome 中安装 Tampermonkey 并添加自定义脚本
icon: server
---

# 如何安装 Tampermonkey 和 WebRTC 调试脚本

## 安装 Tampermonkey

要在 Chrome 中运行自定义脚本，可以方便地使用 **Tampermonkey** 扩展。

前往 Chrome 网上应用店并安装扩展程序：

{% embed url="https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo" %}

安装后，单击右上角的扩展图标并固定**Tampermonkey**。

{% hint style="info" %}
仅需要该扩展程序才能在浏览器中运行脚本。它本身并不能修复 WebRTC 泄漏。
{% endhint %}

## 如何手动添加脚本

对于本指南，请使用 Gist 中的脚本：

* [WebRTC调试脚本](https://gist.github.com/Kr1tos/26585898c08e5222d5edc3d6fad546be)

{% stepper %}
{% step %}
#### 使用脚本打开要点

打开要点链接。

打开脚本文件并复制其完整内容。
{% endstep %}

{% step %}
#### 在 Tampermonkey 中创建一个新脚本

单击 **Tampermonkey** 图标并选择 **创建新脚本**。

删除在编辑器中打开的默认模板。
{% endstep %}

{% step %}
####粘贴脚本代码

将复制的代码从 Gist 粘贴到 Tampermonkey 编辑器中。

使用 **Ctrl + S** 或 **文件 → 保存** 按钮保存更改。
{% endstep %}

{% step %}
#### 检查脚本是否启用

确保新脚本出现在 Tampermonkey 列表中并且具有 **已启用** 状态。
{% endstep %}
{% endstepper %}

## 如何检查脚本是否有效

1. 确保脚本切换已启用。
2. 刷新目标页面。
3. 使用 **F12** 打开 DevTools。
4. 转到**控制台**选项卡。
5、通过`\[TM]`、`\[WebRTC]`、`\[NET]`标签可以方便的过滤输出。

### 应该出现什么日志

脚本启动后，通常会立即出现服务消息：

```
[TM] Network hooks installed
[TM] WebRTC hook installed
```

如果页面创建了`RTCPeerConnection`，WebRTC日志将出现在控制台中：

```
[WebRTC] created
config: { iceServers: [...] }
ICE servers: [...]
```

在候选人聚集期间，本地和远程候选人将可见：

```
[WebRTC] local candidate raw: candidate:...
[WebRTC] local candidate parsed: { ip: "192.168.1.10", port: "52344", type: "host" }

[WebRTC] remote candidate raw: candidate:...
[WebRTC] remote candidate parsed: { ip: "185.123.45.67", port: "3478", type: "srflx" }
```

如果连接到达路由选择，脚本将显示最终路径：

```
[WebRTC] SELECTED PATH (connectionstatechange)
candidate-pair: { ... }
local-candidate: { ip: "10.0.0.2", port: 54012, protocol: "udp", candidateType: "host" }
remote-candidate: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
[WebRTC] REAL REMOTE ENDPOINT: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
```

如果网站通过 `fetch`、`xhr`、`WebSocket` 或 `sendBeacon` 发送 WebRTC 数据，脚本也会显示：

```
[NET][fetch] https://site.example/api
[NET] SDP detected
v=0
o=- 46117317 2 IN IP4 127.0.0.1
...

[NET][ws] wss://site.example/socket
[NET] ICE detected
{"candidate":"candidate:...","sdpMid":"0","sdpMLineIndex":0}
```

### 首先看什么

* `\[TM] WebRTC hook installed` - 脚本加载成功。
* `\[WebRTC] created` - 该页面确实创建了 WebRTC 连接。
* `\[WebRTC] local candidate parsed` - 本地候选者可见。
* `\[WebRTC] remote candidate parsed` - 远程候选者可见。
* `\[WebRTC] REAL REMOTE ENDPOINT` - 最有用的日志。它显示了 WebRTC 选择的最终远程端点。

### 如果日志很少

该脚本添加了两个手动控制台命令：

```javascript
__dumpAllWebRTCSelectedPaths()
__dumpAllWebRTCStats()
```

第一个命令再次打印选定的路径。

第二个显示了 `candidate-pair`、`local-candidate`、`remote-candidate` 和 `transport` 的完整快照。

## 安装后有用的检查

启动脚本后，您可以使用[如何检查WebRTC泄漏](webrtc-leak-check-tools.md)一文中的服务来检查WebRTC行为。

如果您想了解泄漏机制本身，请参阅[WebRTC泄漏的工作原理](how-webrtc-leak-works.md)。



