# Начало работы

API ProxyShard позволяет получать информацию о профиле и заказах, управлять прокси и выполнять другие операции из своих приложений и скриптов.

## Где получить API-ключ

1. В левом нижнем углу нажмите кнопку с тремя точками рядом с профилем.
2. Выберите `Settings`.
3. Откройте вкладку `API`.
4. Нажмите `Copy`, чтобы скопировать ключ.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/proxyshard-api-key_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/proxyshard-api-key_white.png" alt="Получение API-ключа в личном кабинете ProxyShard">
  </picture>
</figure>

{% hint style="warning" %}
Не публикуйте API-ключ и не передавайте его посторонним. Кнопка `Change API Key` создаёт новый ключ. После замены обновите ключ во всех скриптах и интеграциях.
{% endhint %}

## Авторизация

Базовый адрес API: `https://user-api.proxyshard.com`.

Для методов, требующих авторизацию, передавайте API-ключ в заголовке запроса:

```http
Authorization: Bearer <API_KEY>
```

## Спецификация OpenAPI

{% file src="../proxy-shard-user-api.openapi.yaml" %}
Скачать спецификацию OpenAPI ProxyShard
{% endfile %}
