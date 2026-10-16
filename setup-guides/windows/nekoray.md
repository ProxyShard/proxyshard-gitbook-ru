# NekoRay

{% hint style="success" %}
NekoRay поддерживает проксирование TCP- и UDP-трафика в режиме TUN.
{% endhint %}

## Скачивание и запуск

Скачайте архив для Windows со [страницы релизов NekoRay](https://github.com/MatsuriDayo/nekoray/releases), распакуйте его и запустите `nekoray.exe` или `nekobox.exe`. При первом запуске выберите ядро `sing-box`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-github-download_white.png" alt="Загрузка NekoRay с GitHub">
  </picture>
</figure>

## Создание профиля

Щёлкните правой кнопкой мыши по пустой области списка серверов и выберите `New profile`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-main-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-main-new-profile_white.png" alt="Создание нового профиля NekoRay">
  </picture>
</figure>

В списке `Type` выберите `Socks`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-type-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-type-socks_white.png" alt="Выбор типа Socks в NekoRay">
  </picture>
</figure>

Заполните параметры подключения:

1. В поле `Name` укажите любое понятное название.
2. В `Address` и `Port` введите адрес и порт прокси.
3. В разделе `Socks` выберите `Version: 5`.
4. Заполните поля `Username` и `Password`.
5. Нажмите `OK`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-config_white.png" alt="Параметры SOCKS5-прокси в NekoRay">
  </picture>
</figure>

{% hint style="info" %}
Расположение данных подключения описано в [общей инструкции](../getting-started.md).
{% endhint %}

## Подключение

Выберите созданный профиль и включите `Tun Mode` в верхней панели. После запуска трафик системы будет направляться через настроенный прокси.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-tun-mode-enable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-tun-mode-enable_white.png" alt="Включение Tun Mode в NekoRay">
  </picture>
</figure>
