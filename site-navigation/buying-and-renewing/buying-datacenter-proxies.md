---
icon: server
---

# 购买数据中心代理

## 购买代理

购买[数据中心代理](https://dashboard.proxyshard.com/datacenter-proxy)时：

1. 打开 `Datacenter Proxy`。
2. 在 `Proxy region` 中选择代理所在国家/地区。
3. 在 `Billing cycle` 中选择付费周期。
4. 在 `Number of proxies` 中填写代理数量。
5. 如需自动续订订单，请启用 `Auto renew`。
6. 如有需要，请启用 `Enable p0f settings`。
7. 在 `Total slots` 中填写 p0f 插槽数量。
8. 如有优惠码，请将其填入 `Promocode`，然后点击 `Apply`。
9. 确认订单金额，然后点击 `Buy now`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-purchase-form_white.png" alt="代理购买表单">
  </picture>
</figure>

## 支付订单

点击 `Buy now` 后，系统会打开状态为 `Unpaid` 的账单。请核对 `Total amount`，然后点击 `Pay with Wallet`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-invoice-payment_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-invoice-payment_white.png" alt="使用 ProxyShard 余额支付账单">
  </picture>
</figure>

支付后，订单会显示在 `Active products` 和 [`My orders`](https://dashboard.proxyshard.com/products) 中。已付款的订单状态为 `Active`。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-active-products_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-active-products_white.png" alt="有效的代理订单">
  </picture>
</figure>

{% hint style="warning" %}
订单同步需要 1-2 分钟。同步完成后，代理即可使用。
{% endhint %}

## 续订订单

订单支持自动续订和手动续订。

启用 `Auto renew` 后，系统会在付费周期结束前 1-2 小时尝试续订。余额充足时，系统会自动扣款，代理将继续运行。

如果自动续订已关闭或余额不足，订单状态会变为 `On-hold`。如需手动续订，请打开订单，点击 ![](<../../.gitbook/assets/datacenter-renew-button.png>)，然后支付新账单。

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-order-details_white.png" alt="手动续订订单">
  </picture>
</figure>

{% hint style="danger" %}
状态为 `Canceled` 的订单无法续订。订单逾期未支付三天后会进入此状态。
{% endhint %}
