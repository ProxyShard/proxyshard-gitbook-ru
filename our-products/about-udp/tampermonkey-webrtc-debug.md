---
description: Установка Tampermonkey в Chrome и добавление пользовательского скрипта
icon: server
---

# Как установить tampermonkey и скрипт для дебага WebRTC

## Вступление

Tampermonkey позволяет запускать пользовательские скрипты, в нашем сценарии, мы рассмотрим как можно с помощью расширения выяснить, есть ли у ресурса проверка WebRTC.

## Установка Tampermonkey

Перейдите в магазин Chrome и установите расширение:

{% embed url="https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo" %}

После установки нажмите на значок расширений справа сверху и закрепите **Tampermonkey**.

{% hint style="info" %}
Расширение нужно только для запуска скрипта в браузере. Само по себе оно не устраняет утечки WebRTC.
{% endhint %}

## Как добавить скрипт вручную

Для этой инструкции используйте скрипт из Gist:

* [Скрипт для дебага WebRTC](https://gist.github.com/Kr1tos/26585898c08e5222d5edc3d6fad546be)

{% stepper %}
{% step %}
#### Откройте Gist со скриптом

Перейдите по ссылке на Gist.

Откройте файл со скриптом и полностью скопируйте его содержимое.
{% endstep %}

{% step %}
#### Создайте новый скрипт в Tampermonkey

Нажмите на иконку **Tampermonkey** и выберите **Create a new script**.

Удалите стандартный шаблон, который откроется в редакторе.
{% endstep %}

{% step %}
#### Вставьте код скрипта

Вставьте скопированный код из Gist в редактор Tampermonkey.

Сохраните изменения сочетанием **Ctrl + S** или кнопкой **File → Save**.
{% endstep %}

{% step %}
#### Проверьте, что скрипт включен

Убедитесь, что новый скрипт отображается в списке Tampermonkey и находится в статусе **Enabled**.
{% endstep %}
{% endstepper %}

## Как проверить, что скрипт работает

1. Убедитесь, что переключатель у скрипта включен.
2. Обновите нужную страницу.
3. Откройте DevTools через **F12**.
4. Перейдите во вкладку **Console**.
5. Удобно фильтровать вывод по меткам `\[TM]`, `\[WebRTC]` и `\[NET]`.

### Какие логи должны появиться

Сразу после запуска скрипта обычно появляются служебные сообщения:

```
[TM] Network hooks installed
[TM] WebRTC hook installed
```

Если страница создает `RTCPeerConnection`, в консоли появятся логи по WebRTC:

```
[WebRTC] created
config: { iceServers: [...] }
ICE servers: [...]
```

Во время сбора кандидатов будут видны локальные и удаленные кандидаты:

```
[WebRTC] local candidate raw: candidate:...
[WebRTC] local candidate parsed: { ip: "192.168.1.10", port: "52344", type: "host" }

[WebRTC] remote candidate raw: candidate:...
[WebRTC] remote candidate parsed: { ip: "185.123.45.67", port: "3478", type: "srflx" }
```

Если соединение дошло до выбора маршрута, скрипт покажет итоговый путь:

```
[WebRTC] SELECTED PATH (connectionstatechange)
candidate-pair: { ... }
local-candidate: { ip: "10.0.0.2", port: 54012, protocol: "udp", candidateType: "host" }
remote-candidate: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
[WebRTC] REAL REMOTE ENDPOINT: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
```

Если сайт отправляет WebRTC-данные через `fetch`, `xhr`, `WebSocket` или `sendBeacon`, скрипт тоже это покажет:

```
[NET][fetch] https://site.example/api
[NET] SDP detected
v=0
o=- 46117317 2 IN IP4 127.0.0.1
...

[NET][ws] wss://site.example/socket
[NET] ICE detected
{"candidate":"candidate:...","sdpMid":"0","sdpMLineIndex":0}
```

### На что смотреть в первую очередь

* `\[TM] WebRTC hook installed` - скрипт успешно загрузился.
* `\[WebRTC] created` - страница реально создала WebRTC-соединение.
* `\[WebRTC] local candidate parsed` - виден локальный кандидат.
* `\[WebRTC] remote candidate parsed` - виден удаленный кандидат.
* `\[WebRTC] REAL REMOTE ENDPOINT` - самый полезный лог. Он показывает конечную удаленную точку, которую выбрал WebRTC.

### Если логов мало

Этот скрипт добавляет две ручные команды в консоль:

```javascript
__dumpAllWebRTCSelectedPaths()
__dumpAllWebRTCStats()
```

Первая команда повторно выводит выбранные пути.

Вторая показывает полный снимок `candidate-pair`, `local-candidate`, `remote-candidate` и `transport`.

## Полезно проверить после установки

После запуска скрипта можно проверить поведение WebRTC через сервисы из статьи [Через что можно проверить утечку WebRTC](webrtc-leak-check-tools.md).

Если хотите понять сам механизм утечки, смотрите статью [Как работает утечка через WebRTC](how-webrtc-leak-works.md).
