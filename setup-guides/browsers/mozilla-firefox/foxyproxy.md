---
description: Прокси для Mozilla Firefox
---

# FoxyProxy

## Установка расширения FoxyProxy

{% hint style="warning" %}
FoxyProxy работает только с TCP-трафиком.
{% endhint %}

Установите [FoxyProxy Standard](https://addons.mozilla.org/firefox/addon/foxyproxy-standard/) из Firefox Add-ons.

{% embed url="https://addons.mozilla.org/firefox/addon/foxyproxy-standard/" %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-addon-page_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-addon-page_white.png" alt="Страница FoxyProxy Standard в Firefox Add-ons">
  </picture>
</figure>

После установки откройте FoxyProxy и перейдите в настройки расширения.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-disable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-disable_white.png" alt="Переход в настройки FoxyProxy">
  </picture>
</figure>

## Настройка прокси

Откройте раздел `Proxies` и нажмите `Add`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-add-proxy-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-add-proxy-form_white.png" alt="Добавление прокси в FoxyProxy">
  </picture>
</figure>

{% hint style="info" %}
Формат данных и пример заказа описаны в разделе [Начало работы](../../getting-started.md).
{% endhint %}

Укажите название профиля в поле `Title`. Затем выберите тип прокси и заполните поля `Hostname`, `Port`, `Username` и `Password` данными из `Proxy List` вашего заказа. Нажмите `Save`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-proxy-config-filled_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-proxy-config-filled_white.png" alt="Заполненный профиль прокси в FoxyProxy">
  </picture>
</figure>

## Подключение

Откройте FoxyProxy и выберите созданный профиль.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_white.png" alt="Выбор профиля прокси в FoxyProxy">
  </picture>
</figure>

Прокси подключён и готов к работе в Mozilla Firefox.
