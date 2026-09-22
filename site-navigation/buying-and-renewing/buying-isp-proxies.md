---
icon: server
---

# 购买 ISP 代理

{% hint style="info" %}
余额中需要有足够的[资金](../top-up-balance.md)才能支付订单。
{% endhint %}

## 购买代理

购买 [ISP 代理](https://dashboard.proxyshard.com/isp-proxy)时：

1. 打开 `ISP Proxy`。
2. 在 `Proxy region` 中选择代理所在国家或地区。
3. 在 `Billing cycle` 中选择付费周期。
4. 在 `Number of proxies` 中填写代理数量。
5. 如需自动续订订单，请启用 `Auto renew`。
6. 如有需要，请启用 `Enable p0f settings`，并在 `Total slots` 中填写插槽数量。
7. 如有优惠码，请将其填入 `Promocode`，然后点击 `Apply`。
8. 确认订单金额，然后点击 `Buy now`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-purchase-form_white.png" alt="ISP 代理购买表单">
  </picture>
</figure>

## 付款和激活

点击 `Buy now` 后，将打开状态为 `Unpaid` 的账单。确认 `Total amount`，然后点击 `Pay with Wallet`。付款流程与[数据中心代理说明](buying-datacenter-proxies.md#zhi-fu-ding-dan)相同。

付款后，订单会显示在 `Active products` 和 [`My orders`](https://dashboard.proxyshard.com/products) 中。

{% hint style="warning" %}
订单同步通常需要 1-2 分钟，完成后代理即可使用。
{% endhint %}

## 管理和续订订单

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-order-details_white.png" alt="管理 ISP 代理订单">
  </picture>
</figure>

启用 `Auto renew` 后，系统会在当前计费周期结束前 1-2 小时尝试续订订单。余额充足时，系统会自动扣款。

如果关闭自动续订或余额不足，订单状态将变为 `On-hold`。如需手动续订，请打开订单，点击 `Renew`，然后支付账单。

有关 `Status`、`Product tag`、访问凭据、p0f 设置和其他字段的说明，请参阅[订单字段](../../our-products/isp-proxies.md#ding-dan-zi-duan)。

{% hint style="danger" %}
状态为 `Canceled` 的订单无法续订。订单连续三天未付款后会进入此状态。
{% endhint %}
