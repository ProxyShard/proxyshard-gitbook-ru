---
description: Установка, настройка и возможности антидетект-браузера ShardBrowser
icon: browser
---

# ShardBrowser

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-cover_black.svg" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-cover_white.svg" alt="Логотип ShardBrowser">
  </picture>
</figure>

{% hint style="info" %}
ShardBrowser представляет собой антидетект-браузер на базе Chromium от команды ShardX. Каждый профиль получает собственный отпечаток (fingerprint) реального устройства и отдельный прокси, поэтому сайты воспринимают профили как разные компьютеры. Программа распространяется бесплатно и поставляется «как есть». При серьёзных проблемах создайте сообщение об ошибке на [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

Официальный сайт ShardBrowser: [shardbrowser.com](https://shardbrowser.com/).

<figure><img src="../.gitbook/assets/shardbrowser-website.png" alt="Официальный сайт ShardBrowser"><figcaption>Официальный сайт ShardBrowser</figcaption></figure>

## Установка и настройка

### Системные требования для Windows

| Компонент        | Минимум                                | Рекомендуется                                 |
| ---------------- | -------------------------------------- | --------------------------------------------- |
| ОС               | Windows 10 22H2 или Windows 11, 64-бит | Windows 11 64-бит                             |
| Архитектура      | x64 / x86\_64                          | x64                                           |
| Процессор        | Двухъядерный 64-бит, поддержка SSE3    | Четырёхъядерный и выше                        |
| ОЗУ              | 4 ГБ                                   | 8 ГБ (16 ГБ при работе с множеством профилей) |
| Место на диске   | 1 ГБ                                   | От 5 ГБ                                       |
| Среда выполнения | Microsoft Edge WebView2                | Последняя версия                              |

---

### Установка на Windows

Скачайте последнюю версию:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

В разделе <mark style="color:purple;">**Assets**</mark> выберите установщик <mark style="color:purple;">`ShardBrowser.Launcher_<версия>_x64-setup.exe`</mark>. Если нужна версия без установки, скачайте <mark style="color:purple;">`ShardBrowser-Launcher-portable-win-x64.exe`</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-github-release-assets_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-github-release-assets_white.png" alt="Выберите x64-setup.exe в разделе Assets">
  </picture>
  <figcaption>Выберите x64-setup.exe в разделе Assets</figcaption>
</figure>

Запустите скачанный файл. <mark style="color:purple;">Windows SmartScreen</mark> может показать предупреждение. Нажмите <mark style="color:purple;">**More info**</mark>, затем <mark style="color:purple;">**Run anyway**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-windows-smartscreen_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-windows-smartscreen_white.png" alt="SmartScreen - нажмите «Run anyway»">
  </picture>
  <figcaption>SmartScreen: нажмите «Run anyway»</figcaption>
</figure>

### Установка на macOS

Скачайте файл <mark style="color:purple;">`ShardBrowser.Launcher_<версия>_aarch64.dmg`</mark> в разделе <mark style="color:purple;">**Assets**</mark>. Сборка предназначена для Mac с процессорами Apple Silicon.

Откройте `.dmg` и перетащите <mark style="color:purple;">**ShardBrowser Launcher**</mark> в папку <mark style="color:purple;">**Applications**</mark>. Приложение подписано сертификатом Apple Developer ID и нотаризовано, поэтому запускается как обычное приложение macOS.

### Установка на Linux

В разделе <mark style="color:purple;">**Assets**</mark> доступны сборки `.AppImage`, `.deb` и `.rpm`. Для запуска AppImage выдайте файлу разрешение на выполнение:

```bash
chmod +x ShardBrowser.Launcher_<версия>_amd64.AppImage
./ShardBrowser.Launcher_<версия>_amd64.AppImage
```

Пакет `.deb` можно установить командой:

```bash
sudo apt install ./ShardBrowser.Launcher_<версия>_amd64.deb
```

### Первый запуск

После установки и запуска откроется главный экран <mark style="color:purple;">**All profiles**</mark>. Слева находится меню разделов: профили, прокси, отпечатки, расширения, закладки, автоматизация и кабинет ShardX.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="Главный экран ShardBrowser">
  </picture>
  <figcaption>Главный экран ShardBrowser</figcaption>
</figure>

---

### Добавляем прокси

Перейдите в раздел <mark style="color:purple;">**Proxies**</mark> и нажмите <mark style="color:purple;">**+ Add proxies**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-proxies-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-proxies-empty_white.png" alt="Раздел Proxies">
  </picture>
  <figcaption>Раздел Proxies</figcaption>
</figure>

В окне <mark style="color:purple;">**Add proxies**</mark> выберите тип в поле <mark style="color:purple;">**Type for lines without one**</mark> (по умолчанию <mark style="color:purple;">SOCKS5</mark>) и вставьте прокси по одному на строку. Поддерживаемые форматы:

```
host:port
host:port:user:pass
user:pass@host:port
socks5://user:pass@host:port
```

Строки, начинающиеся с `#`, игнорируются. Прокси, которые уже есть в списке (тот же тип, хост, порт, логин и пароль), будут пропущены.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-paste_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-paste_white.png" alt="Вставьте прокси по одному на строку и нажмите «Preview»">
  </picture>
  <figcaption>Вставьте прокси по одному на строку и нажмите «Preview»</figcaption>
</figure>

Нажмите <mark style="color:purple;">**Preview**</mark>. В окне предпросмотра нажмите <mark style="color:purple;">**Test all**</mark>, чтобы проверить прокси перед добавлением. После теста каждый прокси получит статус и страну.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-preview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-preview_white.png" alt="Нажмите «Test all», затем «Add 1 proxy»">
  </picture>
  <figcaption>Нажмите «Test all», затем «Add 1 proxy»</figcaption>
</figure>

Прокси с меткой <mark style="color:purple;">**UDP**</mark> поддерживают <mark style="color:purple;">SOCKS5 UDP</mark>, а значит и <mark style="color:purple;">WebRTC</mark>, что очень полезно при работе с серьёзными антифрод-системами. Если метки <mark style="color:purple;">**UDP**</mark> нет, профиль переходит в режим <mark style="color:purple;">**TCP-only**</mark>: IP не утечёт, однако трафик может выглядеть подозрительно для продвинутых антифрод-систем. Мы крайне советуем использовать [прокси с поддержкой UDP](about-udp/).

Кнопка <mark style="color:purple;">**Select working only**</mark> оставит выбранными только рабочие прокси. Нажмите <mark style="color:purple;">**Add 1 proxy**</mark> - прокси появится в списке.

---

### Создаём первый профиль

Перейдите в раздел <mark style="color:purple;">**All profiles**</mark> и нажмите <mark style="color:purple;">**+ New profile**</mark>. Профиль можно также импортировать из буфера обмена кнопкой <mark style="color:purple;">**Import from clipboard**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-button_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-button_white.png" alt="Раздел All profiles">
  </picture>
  <figcaption>Раздел All profiles</figcaption>
</figure>

Откроется окно <mark style="color:purple;">**New profile**</mark> с вкладками <mark style="color:purple;">**Basics**</mark>, <mark style="color:purple;">**Proxy**</mark>, <mark style="color:purple;">**Fingerprint**</mark> и <mark style="color:purple;">**Extensions**</mark>. На вкладке <mark style="color:purple;">**Basics**</mark> укажите имя профиля. Здесь же можно выбрать папку, теги, цвет, добавить заметку и загрузить файл cookies.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-basics_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-basics_white.png" alt="Укажите имя профиля">
  </picture>
  <figcaption>Укажите имя профиля</figcaption>
</figure>

На вкладке <mark style="color:purple;">**Proxy**</mark> выберите сохранённый прокси из списка. Через <mark style="color:purple;">**+ Add a new proxy**</mark> можно сразу добавить новый.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-proxy_white.png" alt="Выберите прокси для профиля">
  </picture>
  <figcaption>Выберите прокси для профиля</figcaption>
</figure>

На вкладке <mark style="color:purple;">**Fingerprint**</mark> параметры менять не обязательно - ShardBrowser сам подберёт отпечаток под выбранную ОС. При желании выберите <mark style="color:purple;">операционную систему</mark> (macOS, Windows, Linux, Android), конкретный отпечаток, видеокарту, количество ядер, память, частоту обновления и разрешение экрана.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-fingerprint_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-fingerprint_white.png" alt="Настройки отпечатка профиля">
  </picture>
  <figcaption>Настройки отпечатка профиля</figcaption>
</figure>

Нажмите <mark style="color:purple;">**Create profile**</mark>.

---

### Запуск профиля

Профиль появится в списке. Справа открывается карточка профиля: прокси, расширения, заметки, параметры отпечатка, часовой пояс и язык (по умолчанию определяются по прокси). Нажмите <mark style="color:purple;">**Start**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-start_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-start_white.png" alt="Нажмите «Start», чтобы запустить профиль">
  </picture>
  <figcaption>Нажмите «Start», чтобы запустить профиль</figcaption>
</figure>

Браузер запустится с изолированным отпечатком и прокси. На стартовой странице `chrome://shardx` перечислены защиты профиля.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-browser-started_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-browser-started_white.png" alt="Профиль запущен">
  </picture>
  <figcaption>Профиль запущен</figcaption>
</figure>

---

### Возможные проблемы

#### Приложение не запускается

Скорее всего, не установлен <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Скачайте и установите его:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

На оригинальных образах Windows 10/11 WebView2 уже включён. На урезанных сборках он может быть удалён.

## Возможности

* Генерация уникальных отпечатков под <mark style="color:purple;">Windows</mark>, <mark style="color:purple;">macOS</mark> и <mark style="color:purple;">Linux</mark> (navigator, screen, client hints, WebGL / WebGPU и т.д.)
* Шум по отдельным векторам: <mark style="color:purple;">canvas, WebGL, audio, client rects, шрифты, сенсоры</mark>
* Неограниченное число профилей с раскладкой по папкам
* Привязка прокси к профилю (<mark style="color:purple;">SOCKS5 / HTTP / HTTPS</mark>) с автотестом при добавлении
* Локальное **HTTP API** для полной автоматизации
* Управление через **CDP** (Chrome DevTools Protocol) — Puppeteer, Playwright и аналоги
* Экспорт и импорт cookies между профилями
* Отдельный **MCP-сервер**, чтобы профилем мог управлять ИИ-агент

### Отпечатки и антидетект

Для каждого профиля ShardBrowser подставляет согласованный набор параметров: User-Agent, платформу, число ядер и объём памяти (никогда не больше, чем у реальной машины), разрешение экрана, Sec-CH-UA и прочее. Сверху накладывается **шум** по отдельным векторам: canvas, WebGL, audio, client rects, шрифты и сенсоры. Каждый блок шума включается независимо, поэтому отпечаток профиля стабилен внутри сессий, но отличается от других профилей и от вашего реального устройства.

{% hint style="info" %}
Отпечаток генерируется уникальным и не привязан к железу: число ядер CPU и объём RAM подгоняются под хост и не завышаются, экран ограничивается параметрами реального дисплея. Это снижает риск обнаружения нестыковок.
{% endhint %}

### Прокси, QUIC и WebRTC

При каждом запуске профиля, ещё до старта браузера, привязанный прокси проверяется на поддержку UDP-relay (SOCKS5 UDP\_ASSOCIATE):

* если UDP работает, включается <mark style="color:purple;">QUIC</mark>, а WebRTC использует проксированный UDP-relay;
* если UDP недоступен, QUIC отключается, а WebRTC переводится в режим **TCP-only**, чтобы реальный IP не утёк.

Поля часового пояса, локали и геолокации в режиме `auto` также определяются через прокси при запуске.

{% hint style="success" %}
Связка ShardBrowser с нашими [**прокси с поддержкой UDP**](about-udp/) закрывает утечку WebRTC на уровне браузера: UDP-трафик идёт через прокси, а не напрямую с вашего IP. Подробнее читайте в разделе [**О протоколе UDP**](about-udp/).
{% endhint %}

### Автоматизация: локальное API

Внутри приложения запускается локальный HTTP-сервер на <mark style="color:purple;">**127.0.0.1**</mark> (порт по умолчанию **40325**, меняется в _Settings → Automation API_). Он доступен только с вашего компьютера.

Все запросы, кроме `GET /health`, требуют **Bearer-токен** (постоянный JWT из настроек):

```
Authorization: Bearer <token>
```

Кнопка **Regenerate token** в настройках мгновенно меняет секрет: новый токен начинает работать сразу, а старые перестают действовать.

Типичный сценарий автоматизации:

1. `GET /fingerprint/new/{platform}` — получить готовый уникальный отпечаток без сохранения.
2. При необходимости изменить отпечаток, например включить шум по шрифтам или сменить режим WebRTC.
3. `POST /profiles` — создать профиль с этим отпечатком и привязать прокси.
4. `POST /profiles/{id}/start` — запустить профиль и получить **CDP-эндпоинт**.
5. Подключиться к нему как `browserWSEndpoint = cdp.web_socket_debugger_url` в Puppeteer / Playwright.
6. `POST /profiles/{id}/stop` — закрыть профиль.

{% hint style="info" %}
**Временные профили.** `POST /profiles/temporary` создаёт скрытый профиль с флагом `temporary`. После закрытия браузера профиль и его папка данных удаляются автоматически.
{% endhint %}

Полное описание методов с моделями данных и примерами смотрите в [спецификации API ShardX Launcher](https://docs.shardx.com/shardx-launcher-api/binding-and-lifecycle).

### MCP-сервер для ИИ-агентов

В комплекте идёт отдельный **MCP-сервер** (Model Context Protocol). Он позволяет ИИ-клиенту управлять лаунчером через API, а браузером профиля — через CDP. Это отдельный Node-процесс, не часть HTTP API.

Скачать его можно прямо из лаунчера (_Settings → MCP server → Download MCP server_). Для настройки используются две переменные: `SHARDX_API` (базовый URL API) и `SHARDX_TOKEN` (Bearer-токен). MCP-сервер предоставляет:

* **API-инструменты** — обёртки над методами лаунчера для профилей, отпечатков, прокси, папок, cookies, запуска и остановки;
* **браузерные инструменты** поверх CDP — навигацию, выполнение JS, скриншоты, клики, ввод текста, работу со вкладками и ожидания.

{% hint style="warning" %}
CDP (remote-debugging) включается **только** при запуске профиля через API. При запуске из интерфейса отладочный порт не используется.
{% endhint %}
