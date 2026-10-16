# ProxyCap (NetDetour)

{% hint style="success" %}
NetDetour поддерживает проксирование TCP- и UDP-трафика.
{% endhint %}

{% hint style="info" %}
NetDetour является актуальным продолжением ProxyCap. Программа платная, пробный период составляет 30 дней.
{% endhint %}

## Установка

Откройте [страницу загрузки](https://www.proxycap.com/download.html), нажмите `Download NetDetour` и установите программу.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/proxycap-netdetour-website-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/proxycap-netdetour-website-download_white.png" alt="Загрузка NetDetour">
  </picture>
</figure>

## Добавление прокси

1. Нажмите значок `Proxifying Settings` в верхней панели.
2. Откройте вкладку `Proxies`.
3. Выберите тип `SOCKS5` и нажмите `Add...`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/proxycap-netdetour-settings-add-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/proxycap-netdetour-settings-add-proxy_white.png" alt="Добавление SOCKS5-прокси в NetDetour">
  </picture>
</figure>

Заполните форму `New SOCKS5 Proxy Server`:

- `Name`: любое понятное название;
- `Host`: IP-адрес или домен прокси;
- `Port`: порт подключения;
- `Proxy requires authentication`: включите этот пункт;
- `Use Username/Password authentication`: укажите логин и пароль.

Нажмите `OK`, чтобы сохранить сервер.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/proxycap-netdetour-proxy-server-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/proxycap-netdetour-proxy-server-config_white.png" alt="Параметры SOCKS5-прокси в NetDetour">
  </picture>
</figure>

{% hint style="info" %}
Расположение данных подключения описано в [общей инструкции](../getting-started.md).
{% endhint %}

## Создание правила

1. В окне `Proxifying Settings` откройте вкладку `Rules`.
2. Нажмите `New...`.
3. На шаге `Rule Action` выберите `Tunnel through proxy`.
4. В списке `Proxy` укажите добавленное подключение.
5. Нажмите `Next >`, выберите нужные приложения или оставьте правило для всех программ, затем сохраните его.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/proxycap-netdetour-rule-action-wizard_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/proxycap-netdetour-rule-action-wizard_white.png" alt="Настройка правила Tunnel through proxy">
  </picture>
</figure>
