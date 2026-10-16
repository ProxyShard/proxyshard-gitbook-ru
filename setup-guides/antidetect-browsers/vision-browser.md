---
description: Антидетект-браузер с поддержкой UDP-прокси
---

# Vision Browser

{% hint style="success" %}
Vision Browser поддерживает TCP- и UDP-трафик через SOCKS5-прокси.
{% endhint %}

## Установка и регистрация

Откройте [сайт Vision Browser](https://browser.vision/r/ecf2408f-02de-4e4f-bc24-be368ac32325), скачайте приложение и установите его.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-website-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-website-download_white.png" alt="Загрузка Vision Browser">
  </picture>
</figure>

Создайте аккаунт. Эти данные потребуются для входа в приложение.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-sign-up_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-sign-up_white.png" alt="Регистрация в Vision Browser">
  </picture>
</figure>

При оплате тарифа можно использовать промокод `PROXYSHARD` со скидкой 20%.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-plan-promo-code_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-plan-promo-code_white.png" alt="Промокод PROXYSHARD в Vision Browser">
  </picture>
</figure>

## Создание первого профиля

1. Откройте `Profiles`.
2. Перейдите в `Folders` и нажмите `Create folder`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folders-create_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folders-create_white.png" alt="Создание папки профилей в Vision Browser">
  </picture>
</figure>

Укажите название папки и сохраните её.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folder-create-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folder-create-form_white.png" alt="Название папки профилей">
  </picture>
</figure>

В созданной папке нажмите `Create profile`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-profiles-create-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-profiles-create-profile_white.png" alt="Создание профиля Vision Browser">
  </picture>
</figure>

В панели ProxyShard сгенерируйте один прокси в формате SOCKS5 и скопируйте данные подключения.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-single_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-single_white.png" alt="Генерация SOCKS5-прокси в ProxyShard">
  </picture>
</figure>

В настройках профиля Vision откройте вкладку `SOCKS`, вставьте данные прокси, проверьте соединение и нажмите `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-create-profile-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-create-profile-socks_white.png" alt="Настройка SOCKS5-прокси в профиле Vision">
  </picture>
</figure>

<figure><img src="../../.gitbook/assets/vision-folder-profile-created.png" alt="Созданный профиль Vision Browser"><figcaption></figcaption></figure>

## Добавление списка прокси

Откройте вкладку `Proxies` и нажмите `Add proxy`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-add-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-add-proxy_white.png" alt="Добавление прокси в Vision Browser">
  </picture>
</figure>

В панели ProxyShard сгенерируйте список прокси в формате SOCKS5 и скопируйте его.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-list_white.png" alt="Генерация списка SOCKS5-прокси">
  </picture>
</figure>

Вставьте список в поле добавления. После импорта убедитесь, что подключения имеют статус `Online`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-imported-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-imported-list_white.png" alt="Импортированный список прокси в Vision Browser">
  </picture>
</figure>

Чтобы назначить прокси существующему профилю, нажмите значок в столбце `Proxy`.

<figure><img src="../../.gitbook/assets/vision-profiles-proxy-column.png" alt="Столбец Proxy в списке профилей"><figcaption></figcaption></figure>

Выберите `Select proxy`, укажите нужное подключение и выполните проверку.

<figure><img src="../../.gitbook/assets/vision-edit-profile-select-proxy.png" alt="Выбор прокси для профиля Vision"><figcaption></figcaption></figure>

После сохранения прокси появится в строке профиля.

<figure><img src="../../.gitbook/assets/vision-profile-proxy-assigned.png" alt="Прокси назначен профилю Vision"><figcaption></figcaption></figure>

## Проверка WebRTC

Запустите профиль и откройте [ProxyShard IP Checker](https://proxyshard.com/ip-checker). Адреса TCP и WebRTC должны совпадать.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-webrtc-check_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-webrtc-check_white.png" alt="Проверка TCP и WebRTC в профиле Vision Browser">
  </picture>
</figure>
