---
icon: lock-keyhole-open
---

# Почему просто TCP-прокси недостаточно!

Даже если ваш SOCKS5-прокси поддерживает <mark style="color:purple;">UDP</mark>, большинство антидетект-браузеров (в частности, на базе Chromium) не умеют передавать <mark style="color:purple;">WebRTC</mark>-трафик через прокси. Причина – технические ограничения ядра браузера.

\
На сегодняшний день капчи-системы уже вводят усиленную проверку на наличие <mark style="color:purple;">WebRTC</mark>, в качестве примера может выступить <mark style="color:purple;">Discord</mark>, они подключили "<mark style="color:purple;">Hcaptcha-enterprise</mark>", где уже включена проверка на наличие включенного <mark style="color:purple;">WebRTC</mark> у пользователя.
