---
description: Установка ShardBrowser, добавление прокси и запуск первого профиля
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

## Системные требования для Windows

| Компонент        | Минимум                                | Рекомендуется                                 |
| ---------------- | -------------------------------------- | --------------------------------------------- |
| ОС               | Windows 10 22H2 или Windows 11, 64-бит | Windows 11 64-бит                             |
| Архитектура      | x64 / x86\_64                          | x64                                           |
| Процессор        | Двухъядерный 64-бит, поддержка SSE3    | Четырёхъядерный и выше                        |
| ОЗУ              | 4 ГБ                                   | 8 ГБ (16 ГБ при работе с множеством профилей) |
| Место на диске   | 1 ГБ                                   | От 5 ГБ                                       |
| Среда выполнения | Microsoft Edge WebView2                | Последняя версия                              |

---

## Установка на Windows

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

## Установка на macOS

Скачайте файл <mark style="color:purple;">`ShardBrowser.Launcher_<версия>_aarch64.dmg`</mark> в разделе <mark style="color:purple;">**Assets**</mark>. Сборка предназначена для Mac с процессорами Apple Silicon.

Откройте `.dmg` и перетащите <mark style="color:purple;">**ShardBrowser Launcher**</mark> в папку <mark style="color:purple;">**Applications**</mark>. Сборка не нотаризована, поэтому перед первым запуском выполните в терминале:

```bash
xattr -dr com.apple.quarantine "/Applications/ShardBrowser Launcher.app"
```

Также разрешить запуск можно в <mark style="color:purple;">**System Settings**</mark> → <mark style="color:purple;">**Privacy & Security**</mark> → <mark style="color:purple;">**Open Anyway**</mark>.

## Установка на Linux

В разделе <mark style="color:purple;">**Assets**</mark> доступны сборки `.AppImage`, `.deb` и `.rpm`. Для запуска AppImage выдайте файлу разрешение на выполнение:

```bash
chmod +x ShardBrowser.Launcher_<версия>_amd64.AppImage
./ShardBrowser.Launcher_<версия>_amd64.AppImage
```

Пакет `.deb` можно установить командой:

```bash
sudo apt install ./ShardBrowser.Launcher_<версия>_amd64.deb
```

## Первый запуск

После установки и запуска откроется главный экран <mark style="color:purple;">**All profiles**</mark>. Слева находится меню разделов: профили, прокси, отпечатки, расширения, закладки, автоматизация и кабинет ShardX.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="Главный экран ShardBrowser">
  </picture>
  <figcaption>Главный экран ShardBrowser</figcaption>
</figure>

---

## Добавляем прокси

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

Прокси с меткой <mark style="color:purple;">**UDP**</mark> поддерживают <mark style="color:purple;">SOCKS5 UDP</mark>, а значит и <mark style="color:purple;">WebRTC</mark>, что очень полезно при работе с серьёзными антифрод-системами. Если метки <mark style="color:purple;">**UDP**</mark> нет, профиль переходит в режим <mark style="color:purple;">**TCP-only**</mark>: IP не утечёт, однако трафик может выглядеть подозрительно для продвинутых антифрод-систем. Мы крайне советуем использовать [прокси с поддержкой UDP](../our-products/about-udp/).

Кнопка <mark style="color:purple;">**Select working only**</mark> оставит выбранными только рабочие прокси. Нажмите <mark style="color:purple;">**Add 1 proxy**</mark> - прокси появится в списке.

---

## Создаём первый профиль

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

## Запуск профиля

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

## Возможные проблемы

### Приложение не запускается

Скорее всего, не установлен <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Скачайте и установите его:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

На оригинальных образах Windows 10/11 WebView2 уже включён. На урезанных сборках он может быть удалён.
