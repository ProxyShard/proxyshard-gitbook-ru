# V2Box

{% hint style="success" %}
V2Box поддерживает UDP-трафик.
{% endhint %}

## Установка V2Box

Установите V2Box из магазина приложений для вашего устройства.

#### <mark style="color:green;">Android</mark>

{% embed url="https://play.google.com/store/apps/details?id=dev.hexasoftware.v2box" %}

#### <mark style="color:blue;">**iOS**</mark>

{% embed url="https://apps.apple.com/app/v2box-v2ray-client/id6446814690" %}

## Настройка V2Box

1. Откройте вкладку `Configs`.
2. Нажмите `+`, чтобы создать конфигурацию.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-configs-add_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-configs-add_white.png" alt="Добавление конфигурации в V2Box">
  </picture>
</figure>

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-add-manual-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-add-manual-config_white.png" alt="Ручная настройка конфигурации в V2Box">
  </picture>
</figure>

В поле `Protocol` выберите `SOCKS`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-protocol-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-protocol-socks_white.png" alt="Выбор протокола SOCKS в V2Box">
  </picture>
</figure>

Введите название конфигурации в поле `Remarks`. Заполните поля `Address`, `Port`, `Username` и `ID/Password/Key` данными из `Proxy List` вашего заказа, затем нажмите `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-server-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-server-form_white.png" alt="Настройка прокси в V2Box">
  </picture>
</figure>

{% hint style="info" %}
Формат данных и пример заказа описаны в разделе [Начало работы](../getting-started.md).
{% endhint %}

Вернитесь в `Configs`, выберите созданную конфигурацию и используйте `Slide to Connect` для подключения.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-connected_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-connected_white.png" alt="Подключение прокси в V2Box">
  </picture>
</figure>

Проверьте подключение через [Proxy Tester](../../our-products/proxy-tester.md).
