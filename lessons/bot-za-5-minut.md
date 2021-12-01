---
description: >-
  В этом уроке вы узнаете, как с помощью Metabot24 создать бот и протестировать
  его в Telegram.
---

# Бот за 5 минут

{% embed url="https://youtu.be/jZxwloH_nvc" %}

### Создание бота

1. [Зарегистрируйтесь](https://app.metabot24.com/register) на платформе Metabot24, подтвердите электронную почту. Далее войдите в аккаунт.
2. [Создайте](https://app.metabot24.com/bot/create) нового бота, нажав кнопку _**Создать нового...**_

{% hint style="info" %}
&#x20;Рекомендуем также ознакомиться с подробным описанием [Как создать бота](https://metabot.gitbook.io/documentation/nachat-rabotu-s-metabot24/kak-sozdat-bota).
{% endhint %}

* Укажите название бота. Например: "Мой первый бот";
* Остальные опции оставьте без изменений.

![](<../.gitbook/assets/image (45).png>)

* Перейдите на страницу **Главная.**

![](<../.gitbook/assets/izobrazhenie (354).png>)

* Перейдите в раздел **Скрипты**, кликнув по наименованию созданного вами бота.

![](<../.gitbook/assets/izobrazhenie (97).png>)

3\. Создайте новый скрипт в только что созданном боте, нажав на кнопку _**Создать**  **скрипт**_.

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Скрипты](https://metabot.gitbook.io/documentation/panel-upravleniya-botom/skripty).
{% endhint %}

* Укажите название скрипта. Например: "Стартовый сценарий";
* Остальные опции оставьте без изменений.

![](<../.gitbook/assets/image (138).png>)

4\. Откройте редактор скрипта, нажав на кнопку _**Перейти в редактор скрипта**_**,** расположенную напротив только, что созданного вами скрипта.

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Редактор скрипта](https://metabot.gitbook.io/documentation/panel-upravleniya-botom/skripty/redaktor-skripta).
{% endhint %}

![](<../.gitbook/assets/image (154).png>)

5\. Добавьте команду _**Отправить текст**_, нажав на кнопку _**Добавить команду**_ и выбрав ее в открывшемся окне.

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Отправить текст](https://metabot.gitbook.io/documentation/komandy/otpravit-tekst).
{% endhint %}

* Напишите текст сообщения. Например, “Привет, мир! 😀👋🏻”.

![](<../.gitbook/assets/image (19).png>)

6\. ****[Создайте](https://app.metabot24.com/status/create) новый статус, нажав на кнопку _**Создать статус**_ в разделе **Настройки бота ->** [**Статусы**](https://app.metabot24.com/status).

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Статусы](https://metabot.gitbook.io/documentation/panel-upravleniya-botom/statusy).
{% endhint %}

* Введите название. Например, “Первое касание”.

![](<../.gitbook/assets/image (7).png>)

7\. [Создайте](https://app.metabot24.com/route/create) новый маршрут, нажав на кнопку _**Создать маршрут**_ в разделе **Настройки бота ->** [**Маршруты**](https://app.metabot24.com/route)**.**

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Маршруты](https://metabot.gitbook.io/documentation/panel-upravleniya-botom/marshruty).
{% endhint %}

* Введите параметры как показано на изображении ниже;
* В качестве _Названия_ укажите "Приветствие";
* В качестве скрипта, выберите только что созданный вами скрипт;
* В _Регулярном выражении_ слитно напишите точка-звездочка ".\*" без кавычек. Это выражение означает, что бот будет реагировать на любой текст от пользователя;
* В качестве _Статуса_ выберите ранее созданный статус **Первое касание**.

![](<../.gitbook/assets/image (152).png>)

### Запуск бота в Telegram

1. Создайте бот в Telegram при помощи **@BotFather** и скопируйте токен.

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием [Интеграция канала Telegram](https://metabot.gitbook.io/documentation/podklyuchenie-kanalov/telegram).
{% endhint %}

&#x20;  2\. [Создайте](https://app.metabot24.com/bot-channel/create) новый канал в Metabot в разделе **Настройки бота ->** [**Каналы**](https://app.metabot24.com/bot-channel), нажав на кнопку _**Новая привязка**._

{% hint style="info" %}
Рекомендуем также ознакомиться с подробным описанием[ ](https://metarex.gitbook.io/metabot24/podklychenie-kanal/telegram)[Каналы](https://metabot.gitbook.io/documentation/panel-upravleniya-botom/kanaly).
{% endhint %}

* Выберите Telegram в качестве Канала;
* Скопируйте токен, полученный на предыдущем шаге;
* Нажмите **Создать**, чтобы сохранить настройки.

{% hint style="warning" %}
**Внимание!** Нажмите **Вебхук**, чтобы установить связь канала и вашим ботом. Не пропустите этот шаг!
{% endhint %}

### Взаимодействие с ботом

Далее перейдите в приложение Telegram, откройте ваш бот и нажмите кнопку **Запустить/Start**. Если вы все сделали правильно, ваш бот поприветствует вас.

![](<../.gitbook/assets/image (120).png>)

{% hint style="success" %}
Поздравляем вас с созданием вашего первого бота на платформе Метабот24!
{% endhint %}

### Следующие шаги

Воспользуйтесь следующими уроками для решения ваших бизнес-задач:

* [Бот первого касания с распознаванием естественного языка (NLP)](https://metabot.gitbook.io/documentation/lessons/bot-pervogo-kasaniya-s-nlp);
* [Создать бот с меню самоообслуживания](https://metabot.gitbook.io/documentation/lessons/bot-s-menyu-samoobsluzhivaniya).
