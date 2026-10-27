---
description: ShardBrowser 中的设备指纹库
icon: fingerprint
---

# Fingerprints

<mark style="color:purple;">**Fingerprints**</mark> 是真实设备指纹库，ShardBrowser 用它来生成配置文件。每个指纹描述一台具体的机器：操作系统、Chrome 版本、显卡、屏幕、CPU 核心数和内存。

顶部是按系统筛选：<mark style="color:purple;">**All**</mark>、<mark style="color:purple;">**macOS**</mark>、<mark style="color:purple;">**Windows**</mark>、<mark style="color:purple;">**Linux**</mark> 和 <mark style="color:purple;">**Android**</mark>，另有更多 <mark style="color:purple;">**Filters**</mark> 和搜索。指纹卡片上显示屏幕分辨率、核心数和 Chrome 版本。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprints-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprints-list_white.png" alt="Fingerprints 页面">
  </picture>
  <figcaption>Fingerprints 页面</figcaption>
</figure>

<mark style="color:purple;">**GPU mismatch**</mark> 标记表示该指纹声明的显卡在你的电脑上并不存在。这样的配置文件可以正常使用，但浏览器无法实现指纹声明的部分 WebGL 和 WebGPU 功能。详细说明见指纹卡片中的 <mark style="color:purple;">**This computer**</mark> 区块。

点击指纹即可打开其卡片。<mark style="color:purple;">**Details**</mark> 区块列出了操作系统、Chrome 版本、显卡、屏幕、核心数、内存和 <mark style="color:purple;">User agent</mark>。<mark style="color:purple;">**New profile**</mark> 会直接基于该指纹创建配置文件。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprint-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprint-details_white.png" alt="指纹卡片与 New profile 按钮">
  </picture>
  <figcaption>指纹卡片与 New profile 按钮</figcaption>
</figure>
