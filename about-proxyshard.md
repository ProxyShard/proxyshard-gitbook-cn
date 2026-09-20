---
description: ProxyShard 服务与产品简介
icon: question
---

# 什么是 ProxyShard

<mark style="color:purple;">**ProxyShard**</mark> 提供住宅、数据中心、ISP 和移动代理，并配套浏览器操作、检测与自动化工具。数据中心和 ISP 地址只分配给一个客户，不与其他用户共享。UDP、p0f 修改及其他功能的可用性取决于具体产品和地区。

<figure>
  <picture>
    <source srcset=".gitbook/assets/proxyshard-products_black.svg" media="(prefers-color-scheme: dark)">
    <img src=".gitbook/assets/proxyshard-products_white.svg" alt="ProxyShard 产品与工具">
  </picture>
  <figcaption><p>ProxyShard 的代理服务、浏览器工具和检测服务</p></figcaption>
</figure>

***

## 我们的产品

### [<mark style="color:green;">住宅代理</mark>](our-products/residential-proxies/)

来自家庭和移动运营商的 IP 地址，可配置地区、会话类型和连接参数。适合需要丰富地址资源和普通用户网络特征的任务。

### [<mark style="color:orange;">数据中心代理</mark>](our-products/datacenter-proxies.md)

提供独享 IP 的高速静态代理。适合长时间会话，以及需要稳定连接、高速和固定地址的任务。

### [<mark style="color:blue;">ISP 代理</mark>](our-products/isp-proxies.md)

部署在互联网服务提供商网络中的静态地址。它兼具数据中心代理的稳定性和 ISP 网络特征，并只分配给一个客户。

### [<mark style="color:red;">移动代理</mark>](our-products/mobile-proxies.md)

支持选择国家和运营商的移动网络代理。可通过链接切换 IP，具体参数取决于所选套餐和地区。

### [<mark style="color:purple;">ProxyShard Extension</mark>](our-products/proxyshard-extension.md)

适用于 Chrome、Firefox 和 Chromium 浏览器的扩展。可保存代理配置、切换并测试连接，还能通过定时器或快捷键轮换移动代理 IP。

### [<mark style="color:purple;">ShardX Launcher</mark>](our-products/shardx-launcher.md)

用于隔离浏览器配置的现代防关联浏览器，可为每个配置使用一致的指纹和独立代理。支持 Windows、macOS 和 Linux，并提供本地 HTTP API、CDP、Puppeteer、Playwright 以及用于自动化的 MCP 服务器。

### [<mark style="color:purple;">IP Checker</mark>](our-products/ip-checker.md)

用于检测 IP 地址、UDP、FakeISP 特征、WebRTC 行为和浏览器配置参数。可在开始工作前确认连接状态。

### [<mark style="color:purple;">Proxy Tester</mark>](our-products/proxy-tester.md)

检测代理可用性、响应时间、出口 IP 和 UDP 支持。可快速测试单个地址或代理列表。
