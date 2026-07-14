# Proxychain

## Настройка Proxychains4

Установите пакет proxychains4 из репозитория

```bash
apt install proxychains4
```

## **Настройка конфигурации**

Откройте конфигурацию по пути <mark style="color:$info;">**/etc/proxychains4.conf**</mark>, в нем укажите протокол и данные для подключения к прокси

<figure><img src="../../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**С примером настройки прокси вы можете ознакомиться в разделе [Инструкция по настройке](../../getting-started.md)**
{% endhint %}

## **Проверка работы** 

После указания настроек подключения, вы проверить работоспособность через обращение на сайт ifconfig.me

```
proxychains curl ifconfig.me
```

**Если проверка подтвердила смену вашего IP-адреса, то теперь вы можете приступить к использованию ваших прокси!**
