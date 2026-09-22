---
icon: server
---

# Приобретение ISP-прокси

{% hint style="info" %}
Для оплаты заказа на балансе должны быть [средства](../top-up-balance.md).
{% endhint %}

## Покупка прокси

Чтобы приобрести [ISP-прокси](https://dashboard.proxyshard.com/isp-proxy):

1. Откройте раздел `ISP Proxy`.
2. В поле `Proxy region` выберите страну прокси.
3. В поле `Billing cycle` выберите период оплаты.
4. В поле `Number of proxies` укажите количество прокси.
5. Включите `Auto renew`, если хотите автоматически продлевать заказ.
6. При необходимости включите `Enable p0f settings` и укажите количество слотов в поле `Total slots`.
7. Если у вас есть промокод, введите его в поле `Promocode` и нажмите `Apply`.
8. Проверьте стоимость заказа и нажмите `Buy now`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-purchase-form_white.png" alt="Форма покупки ISP-прокси">
  </picture>
</figure>

## Оплата и активация

После нажатия `Buy now` откроется счёт со статусом `Unpaid`. Проверьте сумму в строке `Total amount`, затем нажмите `Pay with Wallet`. Оплата проходит так же, как в [инструкции для датацентр-прокси](buying-datacenter-proxies.md#oplata-zakaza).

После оплаты заказ появится в блоке `Active products` и в разделе [`My orders`](https://dashboard.proxyshard.com/products).

{% hint style="warning" %}
Прокси станут доступны в течение 1-2 минут, пока заказ синхронизируется.
{% endhint %}

## Управление и продление заказа

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-order-details_white.png" alt="Управление заказом ISP-прокси">
  </picture>
</figure>

Если включена функция `Auto renew`, система попытается продлить заказ за 1-2 часа до окончания текущего платёжного периода. При достаточном балансе средства спишутся автоматически.

Если автоматическое продление отключено или на балансе недостаточно средств, заказ получит статус `On-hold`. Для ручного продления откройте заказ, нажмите `Renew` и оплатите выставленный счёт.

Описание `Status`, `Product tag`, данных доступа, настроек p0f и остальных полей приведено в разделе [Поля заказа](../../our-products/isp-proxies.md#polya-zakaza).

{% hint style="danger" %}
Заказ в статусе `Canceled` продлить нельзя. Неоплаченный заказ переходит в этот статус через три дня.
{% endhint %}
