---
description: Сценарии автоматизации профилей ShardBrowser
icon: robot
---

# Automation

Раздел <mark style="color:purple;">**Automation**</mark> позволяет собрать сценарий из последовательности действий: открыть страницу, нажать на элемент, ввести текст, сменить прокси и выполнить другие шаги. Нажмите <mark style="color:purple;">**+ New project**</mark>, чтобы создать сценарий. Готовый проект можно загрузить кнопкой <mark style="color:purple;">**Import**</mark>.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-automation-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-automation-empty_white.png" alt="Раздел Automation">
  </picture>
  <figcaption>Раздел Automation</figcaption>
</figure>

Сценарий собирается из шагов в окне <mark style="color:purple;">**Add a step**</mark>. Шаги разбиты по группам: <mark style="color:purple;">**Profile**</mark>, <mark style="color:purple;">**Proxy**</mark>, <mark style="color:purple;">**Navigation**</mark>, <mark style="color:purple;">**Touch**</mark>, <mark style="color:purple;">**Pointer**</mark>, <mark style="color:purple;">**Keyboard**</mark>, <mark style="color:purple;">**Flow**</mark>, <mark style="color:purple;">**Requests**</mark>, <mark style="color:purple;">**Traffic**</mark>, <mark style="color:purple;">**Data**</mark> и <mark style="color:purple;">**Database**</mark>. Нужный шаг можно найти через поиск.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-automation-add-step_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-automation-add-step_white.png" alt="Окно «Add a step»">
  </picture>
  <figcaption>Окно «Add a step»</figcaption>
</figure>

Например, в группе <mark style="color:purple;">**Profile**</mark> доступны шаги:

| Шаг                    | Что делает                                     |
| ---------------------- | ---------------------------------------------- |
| Temporary profile      | Создаёт профиль, который удалится после выполнения сценария |
| Create profile         | Создаёт постоянный профиль                      |
| Swap proxy (live)      | Меняет прокси без перезапуска браузера          |
| Use profile            | Использует уже существующий профиль             |
| Keep profile           | Сохраняет временный профиль после выполнения сценария |
| Read a profile setting | Читает значение настройки профиля по имени      |
| Delete profile         | Удаляет профиль                                 |

Кнопка <mark style="color:purple;">**Manage modules**</mark> управляет подключёнными модулями шагов.

{% hint style="info" %}
Профилями также можно управлять из своего кода через локальный HTTP API на `127.0.0.1:40325` - статус <mark style="color:purple;">**API on**</mark> показан внизу бокового меню.
{% endhint %}
