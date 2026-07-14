---
description: Установка ShardX Launcher, настройка прокси и запуск первого профиля
icon: browser
---

# ShardX Launcher

{% hint style="info" %}
ShardX Launcher распространяется по лицензии MIT как бесплатный инструмент для личного использования. Программа поставляется «как есть». Мы регулярно выпускаем обновления, но поддержку в лайв-чате не оказываем — при серьёзных проблемах создайте баг-репорт на [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

## Системные требования

### Windows

| Компонент        | Минимум                                          | Рекомендуется                                     |
| ---------------- | ------------------------------------------------ | ------------------------------------------------- |
| ОС               | Windows 10 22H2 или Windows 11, 64-бит           | Windows 11 64-бит                                 |
| Архитектура      | x64 / x86\_64                                    | x64                                               |
| Процессор        | Двухъядерный 64-бит, поддержка SSE3              | Четырёхъядерный и выше                            |
| ОЗУ              | 4 ГБ                                             | 8 ГБ (16 ГБ при работе с множеством профилей)     |
| Место на диске   | 1 ГБ                                             | 5 ГБ+                                             |
| Среда выполнения | Microsoft Edge WebView2                          | —                                                 |

### macOS

| Компонент      | Минимум                              | Рекомендуется               |
| -------------- | ------------------------------------ | --------------------------- |
| ОС             | macOS 11 Big Sur или новее           | Последняя стабильная версия |
| Процессор      | Apple Silicon M1 или новее           | Apple M2 или новее          |
| ОЗУ            | 4 ГБ                                 | 8 ГБ и более                |
| Место на диске | 1 ГБ                                 | 5 ГБ+                       |

{% hint style="warning" %}
Текущая сборка собрана под `aarch64-apple-darwin`. Mac на Intel не поддерживается.
{% endhint %}

---

## Установка на Windows

Скачайте последнюю версию:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

В разделе <mark style="color:purple;">**Assets**</mark> выберите файл <mark style="color:purple;">`.exe`</mark> или <mark style="color:purple;">`.msi`</mark>.

<figure><img src="../.gitbook/assets/shardx-win-download.png" alt=""><figcaption>Выберите .exe или .msi в разделе Assets</figcaption></figure>

Запустите скачанный файл. <mark style="color:purple;">Windows SmartScreen</mark> может показать предупреждение — нажмите <mark style="color:purple;">**Подробнее**</mark>, затем <mark style="color:purple;">**Выполнить в любом случае**</mark>.

<figure><img src="../.gitbook/assets/shardx-win-smartscreen.png" alt=""><figcaption>SmartScreen — нажмите «Run anyway»</figcaption></figure>

Установщик завершит работу за несколько секунд.

<figure><img src="../.gitbook/assets/shardx-win-install-done.png" alt=""><figcaption>Установка завершена</figcaption></figure>

---

## Установка на macOS

Скачайте последнюю версию:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

В разделе <mark style="color:purple;">**Assets**</mark> выберите файл <mark style="color:purple;">`aarch64.dmg`</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-download.png" alt=""><figcaption>Выберите aarch64.dmg в разделе Assets</figcaption></figure>

Откройте скачанный `.dmg` и перетащите <mark style="color:purple;">**ShardX Launcher**</mark> в папку <mark style="color:purple;">**Applications**</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-install-dmg.png" alt=""><figcaption>Перетащите иконку в Applications</figcaption></figure>

### Снятие блокировки Gatekeeper

{% hint style="warning" %}
Этот шаг обязателен. macOS блокирует все неподписанные приложения — без него приложение не откроется.
{% endhint %}

Откройте <mark style="color:purple;">**Терминал**</mark> одним из двух способов:

- <mark style="color:purple;">**Spotlight:**</mark> нажмите `⌘ + Пробел`, введите `terminal`, выберите приложение

<figure><img src="../.gitbook/assets/shardx-mac-find-terminal.png" alt=""><figcaption>Поиск Терминала через Spotlight</figcaption></figure>

- <mark style="color:purple;">**Finder:**</mark> Программы (Applications) -> Утилиты (Utilities) -> Терминал

Вставьте команду и нажмите <mark style="color:purple;">**Enter:**</mark>

```bash
xattr -dr com.apple.quarantine "/Applications/ShardX Launcher.app"
```

<figure><img src="../.gitbook/assets/shardx-mac-xattr-command.png" alt=""><figcaption>Команда выполнится без вывода — это нормально</figcaption></figure>

После этого откройте приложение через <mark style="color:purple;">Spotlight</mark> (`⌘ + Пробел` → `shardx`) или из папки <mark style="color:purple;">Applications</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-open-spotlight.png" alt=""><figcaption>Запуск ShardX через Spotlight</figcaption></figure>

---

## Первый запуск

При первом запуске ShardX скачает браузерный движок с CDN (около 198 МБ, один раз). Подождите завершения загрузки.

<figure><img src="../.gitbook/assets/shardx-win-first-run.png" alt=""><figcaption>Загрузка движка при первом запуске</figcaption></figure>

После загрузки откроется главный экран <mark style="color:purple;">**Browsers**</mark>.

<figure><img src="../.gitbook/assets/shardx-win-ready.png" alt=""><figcaption>Главный экран ShardX Launcher</figcaption></figure>

---

## Добавляем прокси

Перейдите в раздел <mark style="color:purple;">**Proxies**</mark> и нажмите <mark style="color:purple;">**+ New proxy**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-empty.png" alt=""><figcaption>Раздел Proxies</figcaption></figure>

В окне <mark style="color:purple;">**Bulk import proxies**</mark> вставьте прокси по одному на строку. Поддерживаемые форматы:

```
host:port
host:port:user:pass
scheme://host:port
scheme://user:pass@host:port
```

<figure><img src="../.gitbook/assets/shardx-setup-add-proxy.png" alt=""><figcaption>Вставьте прокси по одному на строку</figcaption></figure>

Нажмите <mark style="color:purple;">**Test all**</mark>, чтобы проверить прокси перед импортом.

<figure><img src="../.gitbook/assets/shardx-setup-check-proxy.png" alt=""><figcaption>Нажмите «Test all» для проверки, затем «Import»</figcaption></figure>

После теста каждый прокси получит статус. Прокси с меткой <mark style="color:purple;">**UDP**</mark> поддерживают <mark style="color:purple;">SOCKS5 UDP</mark>, а значит и <mark style="color:purple;">WebRTC</mark> — что очень полезно при работе с серьёзными антифрод-системами. Если метки <mark style="color:purple;">**UDP**</mark> нет, профиль браузера автоматически переходит в режим <mark style="color:purple;">**TCP-only**</mark>: IP не утечёт, однако трафик может выглядеть подозрительно для продвинутых антифрод-систем. Мы крайне советуем использовать [прокси с поддержкой UDP](../our-products/about-udp/).

Нажмите <mark style="color:purple;">**Import**</mark> — прокси появится в списке со статусом <mark style="color:purple;">**Active**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-done.png" alt=""><figcaption>Прокси добавлен</figcaption></figure>

---

## Создаём первый профиль

Перейдите в раздел <mark style="color:purple;">**Browsers**</mark> и нажмите <mark style="color:purple;">**+ New profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profiles-empty.png" alt=""><figcaption>Раздел Browsers</figcaption></figure>

Параметры по умолчанию менять не нужно — ShardX сам сгенерирует уникальный <mark style="color:purple;">отпечаток (fingerprint)</mark>. Обязательно выберите прокси в поле <mark style="color:purple;">**Proxy**</mark> внизу формы.

<figure><img src="../.gitbook/assets/shardx-setup-new-profile.png" alt=""><figcaption>Выберите прокси и нажмите «Create profile»</figcaption></figure>

Нажмите <mark style="color:purple;">**Create profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profile-proxy-check.png" alt=""><figcaption>Профиль создан</figcaption></figure>

---

## Запуск профиля

Нажмите <mark style="color:purple;">**Start**</mark> — браузер запустится с изолированным отпечатком и прокси.

<figure><img src="../.gitbook/assets/shardx-setup-done.png" alt=""><figcaption>Профиль запущен</figcaption></figure>

---

## Возможные проблемы

### Windows: приложение не запускается

Скорее всего, не установлен <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Скачайте и установите его:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

На оригинальных образах Windows 10/11 WebView2 уже включён. На урезанных сборках он может быть удалён.

### macOS: «ShardX Launcher повреждён и не может быть открыт»

Стандартная блокировка <mark style="color:purple;">Gatekeeper</mark>. Следуйте шагам в разделе [Снятие блокировки Gatekeeper](#snyatie-blokirovki-gatekeeper) — там описаны оба способа открыть Терминал и команда для снятия карантина.

---

## Что дальше?

- **Автоматизация:** управляйте профилями через [локальный HTTP API](../our-products/shardx-launcher.md) на `127.0.0.1:40325`
- **MCP-сервер:** скачайте из настроек (<mark style="color:purple;">Settings -> MCP server</mark>) для управления профилями через AI-агента
