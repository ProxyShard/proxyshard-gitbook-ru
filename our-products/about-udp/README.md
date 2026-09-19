---
description: >-
  Зачем нужна поддержка UDP в прокси и как это помогает обходить
  антифрод-системы
icon: shield-exclamation
---

# О протоколе UDP

### **Содержание**

* [Как работает детект через WebRTC](how-webrtc-leak-works.md)
* [Через что можно проверить утечку или работоспособность WebRTC](webrtc-leak-check-tools.md)
* [Почему блокировка WebRTC не спасает от обнаружения](why-blocking-webrtc-doesnt-help.md)
* [Как установить Tampermonkey и скрипт для отладки WebRTC](tampermonkey-webrtc-debug.md)
* [Результаты наших полевых тестов](field-test-results.md)
* [Программные решения для включения WebRTC](webrtc-software-solutions.md)
* [В каких продуктах доступен UDP](#v-kakikh-produktakh-dostupen-udp)
* [FAQ (Частые вопросы)](../../faq-and-support/faq/)

### **Вводная теория**

Современные антифрод-системы используют всё больше способов определить реальный IP-адрес и выявить инструменты, которые маскируют сетевой трафик. Даже если вы используете прокси или <mark style="color:purple;">VPN</mark>, сайт может обнаружить такую маскировку по другим признакам.

Один из таких механизмов связан с <mark style="color:purple;">WebRTC</mark>. Эта технология может отправлять запросы по UDP и раскрывать реальный IP-адрес пользователя, если прокси или клиентское приложение не поддерживает UDP либо направляет такой трафик неправильно.

## В каких продуктах доступен UDP

| Продукт | Поддержка UDP |
| --- | --- |
| [Datacenter](../datacenter-proxies.md) | ✓ Во всех локациях |
| [ISP](../isp-proxies.md) | ✓ Во всех локациях |
| [Mobile](../mobile-proxies.md) | ✓ |
| [Standard Residential](../residential-proxies/standard-residential.md) | ✓ Кроме США; действуют ограничения по портам |
| [Unlimited Residential](../residential-proxies/unlimited-residential-proxy.md) | ✓ Кроме США; действуют ограничения по портам |
| [Premium Residential](../residential-proxies/premium-residential.md) | ✓ Во всех локациях, кроме отдельных городов и устройств macOS/iOS |

Для передачи UDP используйте SOCKS5 и приложение с поддержкой `UDP ASSOCIATE`. Подходящие варианты перечислены в разделе [Программные решения для включения WebRTC](webrtc-software-solutions.md).

Полный список исключений и закрытых портов приведён на странице [Ограничения](../restrictions.md).
