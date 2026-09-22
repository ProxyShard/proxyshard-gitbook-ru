---
icon: fire
---

# ISP прокси

<mark style="color:purple;">ISP прокси</mark>, как и <mark style="color:purple;">Датацентр прокси</mark>, выдаются одному пользователю без скрытого шейринга. Адреса относятся к типу <mark style="color:purple;">IPv4</mark> и поддерживают <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP прокси</mark> сочетают преимущества <mark style="color:purple;">Residential</mark> и <mark style="color:purple;">Datacentre</mark>. Они такие же стабильные и статические, как Datacentre, но используют IP-адреса, зарегистрированные у домашних интернет-провайдеров.

Это делает их подходящим вариантом для Tier-1 сайтов и сервисов, чувствительных к типу <mark style="color:purple;">IP</mark>. Поддержка <mark style="color:purple;">UDP</mark> также позволяет использовать их для WebRTC и других сценариев с UDP-трафиком.

ISP прокси поддерживают подмену сетевого отпечатка <mark style="color:purple;">p0f</mark>.

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

Пошаговая инструкция по покупке и оплате: [Приобретение ISP-прокси](../site-navigation/buying-and-renewing/buying-isp-proxies.md).

Актуальные ограничения продукта приведены на странице [Ограничения](restrictions.md).

## Характеристики

| Параметр            | Значение                              |
| ------------------- | ------------------------------------- |
| Тип IP              | IPv4 (домашний провайдер)             |
| Шеринг              | Нет - один IP на одного пользователя   |
| Лимит подключений   | 2 500 на IP                           |
| [Поддержка UDP](about-udp/) | ✓                             |
| [Поддержка p0f](p0f-spoofing.md) | ✓ (+$0.6 / IP в месяц)   |
| Стоимость           | **$2** / IP в месяц                   |

## Доступные локации

| Страна |
| ------ |
| 🇹🇷 Турция |
| 🇺🇸 США |
| 🇨🇿 Чехия |
| 🇺🇦 Украина |

{% hint style="info" %}
Список локаций постоянно расширяется.
{% endhint %}

## Как приобрести

1. Откройте раздел `ISP Proxy`.
2. В поле `Proxy region` выберите страну.
3. В поле `Number of proxies` укажите количество прокси.
4. Включите `Auto renew`, если заказ нужно продлевать автоматически.
5. При необходимости включите `Enable p0f settings`.
6. В поле `Total slots` укажите, для скольких прокси нужна подмена p0f.
7. Если у вас есть промокод, введите его в поле `Promocode` и нажмите `Apply`.
8. Проверьте стоимость и нажмите `Buy now`.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/isp-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/isp-purchase-form_white.png" alt="Покупка ISP-прокси">
  </picture>
</figure>

Оплата и продление заказа описаны в инструкции [Приобретение ISP-прокси](../site-navigation/buying-and-renewing/buying-isp-proxies.md).

{% hint style="info" %}
После оплаты подождите 1-2 минуты, пока заказ синхронизируется и прокси начнут работать.
{% endhint %}

## Поля заказа

<figure>
  <picture>
    <source srcset="../.gitbook/assets/isp-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/isp-order-details_white.png" alt="Поля заказа ISP-прокси">
  </picture>
</figure>

* `Status` показывает состояние заказа: `Active`, `On-hold` или `Canceled`.
* `Product tag` задаёт метку для поиска заказа в списках.
* `User ID` используется для внутренней идентификации заказа и может потребоваться при обращении в поддержку.
* `Proxy Region` показывает выбранную страну.
* `p0f slots` показывает количество активных слотов p0f и их изменение в следующем платёжном периоде.
* `Username` и `Password` содержат данные авторизации. Кнопка `Regenerate` создаёт новый пароль, после чего старые строки подключения перестают работать.
* `Billing cycle`, `Next due date`, `Price` и `Next charge` показывают срок аренды и данные следующего платежа.
* `Auto-renew proxy` управляет автоматическим продлением. Те же настройки доступны через `Manage renewal`.
* Кнопки `p0f` и `Buy p0f slots` открывают настройки подмены отпечатка и покупку дополнительных слотов.
* В блоке `Proxy List` можно выбрать `HTTP` или `SOCKS5`, изменить формат строки, скопировать список через `Copy all` или выгрузить его через `Export All`.

{% hint style="danger" %}
Заказ со статусом `Canceled` восстановить нельзя. Этот статус присваивается через три дня после неоплаты.
{% endhint %}

## Для каких задач подходит

Любые криптобиржи, Polymarket, стабильные сессии web scraping, SEO мониторинг, e-commerce мониторинг цен, проверка маркетплейсов, ad verification, brand monitoring, тестирование сайтов из домашнего провайдерского ASN, QA авторизации и пользовательских сценариев, мониторинг доступности сайтов, account management.

## Плюсы и минусы ISP прокси

#### <mark style="color:green;">Плюсы:</mark>

* **Настоящие ISP адреса** - IP числятся за реальными домашними интернет-провайдерами (в геолокационных базах тип ASN - провайдер, а не хостинг)
* **Надёжные операторы домашней связи**
* **Широкий канал с минимальной задержкой**
* **Статические адреса в одни руки** - IP не меняется на протяжении аренды
* **Поддержка p0f и UDP**

#### <mark style="color:red;">Минусы:</mark>

* **Цена** - выше, чем у Datacenter прокси
* **Количество доступных локаций** - крайне сложная интеграция с реальными провайдерами, но мы постоянно расширяем список

{% hint style="info" %}
Примеры настройки прокси собраны в разделе [Инструкция по использованию](../setup-guides/getting-started.md).
{% endhint %}
