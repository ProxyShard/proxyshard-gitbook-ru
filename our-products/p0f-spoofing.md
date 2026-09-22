---
icon: fingerprint
---

# Подмена сетевого отпечатка (p0f)

## Что такое p0f и почему он важен

У каждого устройства в сети есть свой цифровой отпечаток на уровне <mark style="color:$primary;">TCP/IP</mark>, который называется <mark style="color:$primary;">**p0f**</mark>. Он формируется из параметров сетевого стека: MSS, TSval, TTL, TCP options, Window size, TOS и других. У Windows, macOS, Linux, iOS и Android эти параметры отличаются, и антифрод системы это знают.

Как работает проверка на стороне сайтов:

1. Сайт смотрит <mark style="color:$primary;">**User-Agent**</mark>, <mark style="color:$primary;">**TLS-отпечаток**</mark> и другие клиентские параметры, чтобы определить, с какой ОС зашёл пользователь
2. Параллельно анализируется <mark style="color:$primary;">**сетевой слой**</mark> соединения, а именно <mark style="color:$primary;">TCP/IP-отпечаток</mark>, который прокси-сервер отправляет вместе с вашим трафиком
3. Если браузер говорит "я Windows 11", а TCP/IP-отпечаток выдаёт <mark style="color:$primary;">Linux</mark>, антифрод-система фиксирует несоответствие

**Проблема всех прокси сервисов -** Все Datacenter и ISP прокси работают на Linux-серверах. Это значит, что в 99% случаев ваш сетевой отпечаток будет Linux, хотя вы заходите с Windows или macOS. Для антифрода это прямой сигнал, что используется прокси.

## Как это решает ProxyShard

Мы добавили возможность **подмены p0f-отпечатка** прямо из личного кабинета. Вы выбираете нужную ОС, и прокси-сервер начинает отправлять сетевые пакеты с соответствующим TCP/IP-отпечатком.

Доступные варианты подмены:

| Значение       | Описание                       |
| -------------- | ------------------------------ |
| **Unset**      | Отпечаток по умолчанию (Linux) |
| **Windows 10** | Отпечаток Windows 10           |
| **Windows 11** | Отпечаток Windows 11           |
| **Mac OS**     | Отпечаток macOS                |
| **Linux**      | Отпечаток Linux                |
| **iOS**        | Отпечаток iOS                  |
| **Android**    | Отпечаток Android              |

### ISP и Datacenter прокси

Откройте заказ, нажмите `p0f` и выберите нужную ОС для каждого IP. Настройка работает одинаково для ISP и Datacenter прокси.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-datacenter-isp_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-datacenter-isp_white.png" alt="Настройка p0f для ISP и Datacenter прокси">
  </picture>
</figure>

### Мобильные прокси

В поле `Signature` выберите ОС, отпечатку которой должен соответствовать прокси. После изменения настройки перезапустите прокси кнопкой `Restart`.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-mobile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-mobile_white.png" alt="Выбор сетевого отпечатка для мобильного прокси">
  </picture>
</figure>

Подмена p0f доступна не во всех мобильных локациях. Актуальный список приведён на странице [Ограничения](restrictions.md).

### Premium Residential

В Premium Residential параметр `Device OS` фильтрует прокси по операционной системе устройства. Это фильтрация пула, а не подмена сетевого отпечатка.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-premium-residential_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-premium-residential_white.png" alt="Фильтрация Premium Residential по Device OS">
  </picture>
</figure>

Доступность `Device OS` зависит от локации. Подробности приведены на странице [Ограничения](restrictions.md).

{% hint style="warning" %}
Перед сменой p0f обязательно закройте все соединения через прокси. Прокси не будет работать, пока старые соединения не будут закрыты. После смены p0f подождите 2-3 минуты и только потом подключайтесь.
{% endhint %}

## Реальные результаты

По промежуточным тестам видно серьёзное улучшение прохождения антифрод-проверок. Один из подтверждённых кейсов:

{% hint style="success" %}
**Google-аккаунты:** совместно с разработчиком [Vision Browser](../setup-guides/antidetect-browsers/vision-browser.md) мы проверили регистрацию Google без модификации отпечатка браузера. На чистом профиле без подмены p0f система сразу предлагает верификацию через QR-код. С подменой p0f на Windows 10/11 QR-проверка не появляется, и Google запрашивает верификацию по номеру телефона - это подтверждает отсутствие детекта прокси.
{% endhint %}

Те, кто работает с регистрацией Google, знают, что без "поломки" отпечатка на десктопе получить верификацию по номеру невозможно, система всегда будет просить QR. Подмена p0f решает эту проблему на сетевом уровне.

## Рекомендуемая связка

Для максимального результата рекомендуем использовать:

* [**Vision Browser**](../setup-guides/antidetect-browsers/vision-browser.md) (антидетект-браузер с поддержкой UDP)
* **ISP прокси от ProxyShard** с включённой подменой p0f

Эта связка закрывает все уровни проверки: браузерный отпечаток (Vision) + сетевой отпечаток (p0f) + чистый IP от домашнего провайдера (ISP).

## Где доступно

Подмена p0f и фильтрация устройств доступны на следующих продуктах:

* [Датацентр прокси](datacenter-proxies.md)
* [ISP прокси](isp-proxies.md)
* [Мобильные прокси](mobile-proxies.md)
* [Premium Residential](residential-proxies/premium-residential.md) - фильтрация устройств по параметру [Device OS](residential-proxies/#nastroika-proksi), без подмены p0f

{% hint style="warning" %}
На некоторых [мобильных прокси](mobile-proxies.md) подмена p0f недоступна. Полный список ограничений смотрите на странице [Ограничения](restrictions.md).
{% endhint %}
