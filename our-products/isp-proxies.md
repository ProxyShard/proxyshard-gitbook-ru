---
icon: fire
---

# ISP прокси

<mark style="color:purple;">ISP прокси</mark> как и <mark style="color:purple;">Датацентр</mark> выдаются в одни руки, никакого шейринга (больше одного пользователя за адресом) и другой формы обмана. Адреса относятся к типу <mark style="color:purple;">IPv4</mark> и имеют поддержку <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP прокси</mark> имеют все плюсы, как у <mark style="color:purple;">Residential</mark> прокси и <mark style="color:purple;">Datacentre</mark>. Они такие же стабильные и статические, как <mark style="color:purple;">Datacentre</mark>, но при этом используют IP-адреса, зарегистрированные на домашних Интернет-провайдера, как у <mark style="color:purple;">Residential</mark> прокси.

Это делает их одним из лучших вариантов для работы с Tier-1 сайтами и сервисами, чувствительными к типу <mark style="color:purple;">IP</mark>. Но с поддержкой <mark style="color:purple;">UDP</mark> они становятся абсолютно не детектируемые.\
\
Недавнее обновление на <mark style="color:purple;">ISP</mark> прокси добавило возможно смены отпечатка (<mark style="color:purple;">p0f</mark>)

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

## Характеристики

| Параметр            | Значение                              |
| ------------------- | ------------------------------------- |
| Тип IP              | IPv4 (домашний провайдер)             |
| Шеринг              | Нет - один IP на одного пользователя   |
| Лимит подключений   | 2 500 на IP                           |
| Поддержка UDP       | ✓                                     |
| Поддержка p0f       | ✓ (+$0.6 / IP в месяц)               |
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

## **Как они работают?**

В самом заказе вы можете обнаружить несколько важных пунктов и опций, рассмотрим их:

Приобрести вы можете на странице [ISP proxy](https://dashboard.proxyshard.com/en/isp-proxy), в нем вам требуется указать <mark style="color:purple;">Страну</mark>, <mark style="color:purple;">Срок аренды</mark> и <mark style="color:purple;">Количество</mark>. При необходимости можете активировать <mark style="color:purple;">Auto renew</mark>, для автоматического продления.

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
После приобретения прокси начнут работать в течении 1-2 минут, так как требуется синхронизация базы данных с сервером прокси.
{% endhint %}

## Описание полей заказа

Рассмотрим поля <mark style="color:purple;">Заказа</mark>:

<mark style="color:purple;">User ID</mark> - Это User используется для внутренней идентификации вашего заказа, иногда мы его запрашиваем при обращении в техническую поддержку.

<mark style="color:purple;">Status</mark> - Статус заказа, может иметь статусы:

* <mark style="color:green;">**Active**</mark> - Активный заказ
* <mark style="color:orange;">**On-Hold**</mark> - Ожидание оплаты заказа при истечении срока аренды
* <mark style="color:red;">**Cancelled**</mark> - Отменённый заказ

{% hint style="danger" %}
Восстановлению заказы со статусом "<mark style="color:$danger;">**Cancelled**</mark>" после трех дней с момента окончания аренды **невозможна**.
{% endhint %}

<mark style="color:purple;">Price</mark> - Стоимость продукта в месяц

<mark style="color:purple;">Username</mark> - Логин прокси

<mark style="color:purple;">Password</mark> - Пароль прокси

<mark style="color:purple;">Next Due Date</mark> - Следующая дата списания

<mark style="color:purple;">Copy proxy</mark> - Кнопка для копирования прокси в буфер обмена

<mark style="color:purple;">HTTP/SOCKS</mark> - Выбор типа протокола прокси

<mark style="color:purple;">Re-generate</mark> - Смена пароля на прокси

<mark style="color:purple;">Auto renew</mark> - переключатель для активации/деактивации продления продукта каждый месяц <mark style="color:purple;">(средства списываются с баланса аккаунта в срок, указанный при приобретении)</mark>

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
О том как можно настроить прокси вы можете в нашем разделе "[Инструкция по использованию](../setup-guides/getting-started.md)"
{% endhint %}
