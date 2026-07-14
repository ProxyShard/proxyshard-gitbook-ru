# ClashX

{% hint style="success" %}
Данное решение поддерживает туннелирование по UDP!
{% endhint %}

## Настройка **ClashX**

Вам необходимо перейти на официальный GitHub проекта ClashX и скачать необходимую версию архива для вашей ОС. В примере приведена настройка на ОС Windows ([Clash.for.Windows-0.20.39-win.7z](https://github.com/lantongxue/clash_for_windows_pkg/releases/download/0.20.39/Clash.for.Windows-0.20.39-win.7z)).

{% embed url="https://github.com/lantongxue/clash_for_windows_pkg/releases" %}

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

## **Запуск ClashX**

Затем необходимо распаковать архив и запустить от имени _<mark style="color:red;">**администратора**</mark>_ "Clash for Windows.exe" как приведено на примере ниже:

<figure><img src="../../.gitbook/assets/image (172).png" alt="" width="563"><figcaption><p>Распаковка архива на рабочий стол</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (162).png" alt="" width="375"><figcaption><p>Запуск от имени администратора</p></figcaption></figure>

## **Настройка программы**

После запуска программы необходимо перейти в "<mark style="color:purple;">Profiles</mark>" и открыть редактор файла <mark style="color:purple;">config.yaml</mark>

<figure><img src="../../.gitbook/assets/image (159).png" alt="" width="375"><figcaption></figcaption></figure>

## **Настройка конфигурационного файла**

Приведите конфигурацию файла как в примере ниже, указав ваши прокси из заказа:

```yaml
proxies:
  - name: "ProxyShard-Germany-testname"
    type: socks5
    server: 123.123.123.123
    port: 1234
    username: proxy_login
    password: password_login
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

В конечно итоге у вас должно получится примерно так:

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="563"><figcaption><p>Пример конфигурации</p></figcaption></figure>

{% hint style="info" %}
**С примером настройки прокси вы можете ознакомиться в разделе [Инструкция по настройке](../getting-started.md)**
{% endhint %}

<pre><code>proxies:
  - name: "ProxyShard-Germany-testname"       | Тут вы задаете имя прокси
    type: socks5                              | Тип протокола 
    server: 123.123.123.123                   | Адрес или домен прокси 
    port: 1234                                | Порт прокси
    username: proxy_login                     | Логин прокси                    
    password: password_login                  | Пароль прокси 
    udp: true                                  
proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname              

rules:
  - PROCESS-NAME,<a data-footnote-ref href="#user-content-fn-1">chrome.exe</a>,Auto   | Выбор определенного приложения для проксирования
  - MATCH,DIRECT      | В нашем примере  используется браузер хрома,
                      | но это может быть любое ваше приложение, например discord.exe  
                      | - MATCH,DIRECT : Указывет, что весь трафик который не является хромом
                      | будет перенаправлен не на прокси, а на ваш основной интерфейс               
</code></pre>

## **Проверка конфигурации**

После настройки конфигурации, вам необходимо открыть "Proxies" и выбрать опцию "Global" и произвести проверку вашего настроенного конфига из 4 пункта.

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="563"><figcaption></figcaption></figure>

Если проверка не прошла и у вас "Failed", то сверьтесь с конфигурационным файлом и убедитесь, что все указанные данные от прокси верно введены. Если настройки верны, вы получите успешный вывод проверки как на скриншоте снизу.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

## **Установка и включение TAP-Интерфейса**

Далее перейдите на "General" и произведите установку TAP-интерфейса на свой компьютер, он создаст новый интерфейс, к которому будет привязана прокси.

После установки TUN-интерфейса вам необходимо включить TUN Mode, как на скриншоте в 4-й рамке

<figure><img src="../../.gitbook/assets/image (163).png" alt="" width="563"><figcaption></figcaption></figure>

## **Проверка работоспособности**

Если все успешно запустилось, вы можете открыть ваше интересующее приложение, для которого вы настраивали конфиг (4 пункт) и можно радоваться работе ваших программ с возможностью проксирования UDP траффика!

В нашем примере проксирование производилось Chrome и мы можем проверить, на [чекерах](../../our-products/about-udp/webrtc-leak-check-tools.md).

<figure><img src="../../.gitbook/assets/image (164).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (165).png" alt="" width="563"><figcaption></figcaption></figure>

Если проверка или проксирование [не работает](../../faq-and-support/faq/proxy-not-working.md), убедитесь, что вы точно запустили ClashX от имени администратора и с 4 по 6 пункт выполнено верно.

## **Дополнительно. Добавление множества прокси и переключение между ними**

Вам необходимо, для возможности быстрого переключения между прокси, дополнить новыми прокси конфигурацию из пункта 4. Имена "ProxyShard-DE-testname1" являются произвольными и можно указать на ваш выбор.

Главным моментом, после добавления, является указание прокси также и для "proxy-group", как продемонстрировано ниже:

```yaml
proxies:
  - name: "ProxyShard-DE-testname1"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true
    
  - name: "ProxyShard-NL-testname2"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

  - name: "ProxyShard-RO-testname3"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-DE-testname1
      - ProxyShard-NL-testname2
      - ProxyShard-RO-testname3

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

Если вы все верно указали, у вас появятся дополнительные точки подключения в "Proxies" и в зависимости от выбранного профиля настроек (просто нажать на любую), будет выполнятся подключение.

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

[^1]: приложение для проксирования
