---
icon: git-alt
---

# Программные решения для включения WebRTC

#### Для полноценной работы WebRTC требуется программное обеспечение с поддержкой UDP ASSOCIATE.

Примеры поддерживаемого софта для разных операционных систем:

<mark style="color:purple;">**Антидетект-браузеры:**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/vision-browser.md): доступное и надёжное решение среди платных браузеров с поддержкой UDP, QUIC, Smart Fingerprint и других полезных функций. Более 60% команд на нашем сайте выбирают именно его.

{% hint style="success" %}
Связка наших [ISP Proxy](https://dashboard.proxyshard.com/en/isp-proxy) и браузера [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) является одним из рекомендуемых вариантов для работы с UDP через прокси. ISP Proxy также поддерживает смену сетевого отпечатка [p0f](../p0f-spoofing.md).
{% endhint %}

* [<mark style="color:$tint;">ShardX</mark>](../shardx-launcher.md): наше решение с открытым исходным кодом, большим выбором профилей и корректной поддержкой UDP и QUIC.

<mark style="color:purple;">**Windows:**</mark>

* ProxiFyre + Windows Packet Filter
* Win2Socks
* Netch
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)

<mark style="color:purple;">**Linux:**</mark>

* proxychains-NG + go-tun2socks
* redsocks-ng

<mark style="color:purple;">**Android:**</mark>

* Clash for Android
* SocksDroid
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)
* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
Актуальный список приложений доступен в [Инструкции по использованию](../../setup-guides/getting-started.md).
{% endhint %}
