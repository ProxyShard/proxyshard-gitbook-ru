# v2rayN GUI

{% hint style="success" %}
Данное решение поддерживает туннелирование по UDP!
{% endhint %}

## Настройка v2rayN.

Перейдите по [ссылке](https://github.com/2dust/v2rayN/releases) для загрузки V2rayN

{% embed url="https://github.com/2dust/v2rayN/releases" %}

<figure><img src="../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

Или скачайте пакет через консоль

```bash
wget https://github.com/2dust/v2rayN/releases/download/7.14.12/v2rayN-linux-64.deb
```

## **Установка и запуск**

Произведите установку скаченного пакета через "<mark style="color:purple;">Discover</mark>" или установите через командную строку

<figure><img src="../../../.gitbook/assets/Image00001 (11).PNG" alt=""><figcaption></figcaption></figure>

```bash
apt install ./v2rayN-linux-64.deb
```

Затем запустите приложение через "<mark style="color:purple;">Пуск</mark>" или командую строку

<figure><img src="../../../.gitbook/assets/Image00002 (12).PNG" alt=""><figcaption></figcaption></figure>

{% code fullWidth="false" %}
```
v2ray
```
{% endcode %}

## **Настройка профиля** 

Создайте новую конфигурация указав SOCKS / HTTP в качестве протокола подключения

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**С примером настройки прокси вы можете ознакомиться в разделе [Инструкция по настройке](../../getting-started.md)**
{% endhint %}

## **Настройка профиля подключения**

Скопированные прокси из заказа вставьте в соответствующие поля, обязательно укажите ядро конфигурации (<mark style="color:purple;">Xray</mark> или <mark style="color:purple;">SingBox</mark>) и сохраните настройки.

<figure><img src="../../../.gitbook/assets/Image00003 (6).PNG" alt=""><figcaption></figcaption></figure>

## Запуск клиента

Запустите клиент, включив <mark style="color:purple;">Tun</mark> режим.

<figure><img src="../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

**Готово! Теперь вы можете полноценно использовать прокси, туннелируя весь трафик на прокси.**
