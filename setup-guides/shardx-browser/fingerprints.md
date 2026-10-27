---
description: Библиотека отпечатков устройств в ShardBrowser
icon: fingerprint
---

# Fingerprints

Раздел <mark style="color:purple;">**Fingerprints**</mark> - это библиотека отпечатков реальных устройств, из которых ShardBrowser собирает профили. Каждый отпечаток описывает конкретную машину: операционную систему, версию Chrome, видеокарту, экран, количество ядер и объём памяти.

Вверху находятся фильтры по системе: <mark style="color:purple;">**All**</mark>, <mark style="color:purple;">**macOS**</mark>, <mark style="color:purple;">**Windows**</mark>, <mark style="color:purple;">**Linux**</mark> и <mark style="color:purple;">**Android**</mark>, а также дополнительные <mark style="color:purple;">**Filters**</mark> и поиск. На карточке отпечатка указаны разрешение экрана, число ядер и версия Chrome.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprints-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprints-list_white.png" alt="Раздел Fingerprints">
  </picture>
  <figcaption>Раздел Fingerprints</figcaption>
</figure>

Метка <mark style="color:purple;">**GPU mismatch**</mark> означает, что отпечаток заявляет видеокарту, которой нет на вашем компьютере. Такой профиль работает, но часть возможностей WebGL и WebGPU, заявленных отпечатком, браузер выполнить не сможет. Подробное объяснение показывается в карточке отпечатка, в блоке <mark style="color:purple;">**This computer**</mark>.

Нажмите на отпечаток, чтобы открыть его карточку. В блоке <mark style="color:purple;">**Details**</mark> указаны ОС, версия Chrome, видеокарта, экран, ядра, память и <mark style="color:purple;">User agent</mark>. Кнопка <mark style="color:purple;">**New profile**</mark> создаёт профиль сразу на основе этого отпечатка.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprint-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprint-details_white.png" alt="Карточка отпечатка, кнопка «New profile»">
  </picture>
  <figcaption>Карточка отпечатка, кнопка «New profile»</figcaption>
</figure>
