---
icon: clipboard-list
---

# Инструкция по настройке

## **Добавление списка прокси из заказа в программы**

Для добавление прокси в разные программы, вам необходимо открыть ваш [заказ](https://dashboard.proxyshard.com/products) на сайте и скопировать прокси:

{% hint style="warning" %}
**Обратите внимание, что во всех примерах, подключение производится через **<mark style="color:purple;">**SOCKS5**</mark>**.** \
\
**Для того чтобы узнать порт подключения для:**\
\
<mark style="color:purple;">**Datacentre\ISP**</mark> - установите переключать на <mark style="color:purple;">SOCKS5</mark> в поле <mark style="color:purple;">Proxy list</mark>

<p align="center"><img src="../.gitbook/assets/image (40).png" alt=""></p>

<mark style="color:purple;">**Residential proxy**</mark> - В настройках заказа указать "<mark style="color:purple;">Protocol</mark>" - <mark style="color:purple;">SOCKS5</mark>

<p align="center"><img src="../.gitbook/assets/image (42).png" alt="" data-size="original"></p>

<mark style="color:purple;">**Mobile proxy**</mark> - Не требуют дополнительных операций в заказе, подключение по порту работает как по <mark style="color:purple;">HTTP</mark> так и по <mark style="color:purple;">SOCKS5</mark>
{% endhint %}

## Пример для <mark style="color:purple;">Датацентр/ISP</mark> прокси

Откройте [заказ](https://dashboard.proxyshard.com/products) и скопируйте прокси из <mark style="color:purple;">Proxy List</mark>.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

212.14.123.184 - IP адрес подключения к прокси

22334 - Port подключения к прокси

KDKKKEI - Login подключения прокси

KDKKEIID3 - Password прокси

## Пример для <mark style="color:purple;">Резидентских прокси</mark>:

Укажите требуемые параметры прокси, например страну/протокол и нажмите "<mark style="color:purple;">Generate proxy</mark>"

<figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

Скопируйте полученные прокси из <mark style="color:purple;">Proxy List</mark> или скопируйте отдельные поля подключения, если программа не поддерживает вставку строкой. 

Ниже приведен скриншот, какое из полей отвечает за "Server":"Port":"Login":"Password"

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
