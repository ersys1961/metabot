---
description: Обращение к боту из внешних систем
---

# Bot API

### Концепция

Бот представляет из себя независимое приложение со собственной бизнес-логикой, моделью данных и состоянием диалога.

Для того чтобы управлять поведением бота из внешних систем вам необходимо запланировать работу (job) с помощью Bot API.

Работа это гибкий механизм, который позволяет реализовать практически любую задачу от самых простых (например, обновить данные пользователя или отправить пользователю текстовое уведомление) до более сложных (например, произвести обработку входящих данных перед их передачей пользователю).

Гибкость достигается это за счет использования встроенного языка программирования JavaScript и системы триггеров.

Сначала в боте на платформе Metabot вы создаете необходимые шаблон сценария диалога и код обработки входных данных, а затем с помощью Bot API планируете работу, которая принимает входные данные и в нужный вам момент передает их в ранее созданные алгоритмы обработки и шаблон сценария.

Шаблон сценария диалога может содержать любую последовательность команда, которую необходимо отправить конечному пользователю (или пользователям) в коммуникационный канал. А алгоритм обработки может содержать любые логику от заполнения данных до обращения к внешним API.

Таким образом работа с API бота из внешних систем представляет обращение к хранимым процедурам бота, которые вы создаете в интерфейсе веб-конструктора.

### Доступ к API

Swagger доступен по адресу: [https://app.metabot24.com/api/docs](https://app.metabot24.com/api/docs)

Чтобы получить доступ, достаточно зарегистрировать любой аккаунт на платформе [https://app.metabot24.com](https://app.metabot24.com), затем создать бот и перейти в раздел пользователей бота [https://app.metabot24.com/user](https://app.metabot24.com/user) и там создать API пользователя.

Ниже описан основной метод работы с ботом.

{% swagger baseUrl="https://test.cakes.com" path="/bots/{botId}/jobs/schedule" method="post" summary="Schedule" %}
{% swagger-description %}
Основной метод для планирования в боте работы.
{% endswagger-description %}

{% swagger-parameter in="path" name="botId" type="number" %}
ID вашего бота
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authentication" type="string" %}
Ваш токен аутентификации. Настраивается в панели администратора в разделе "Пользователи бизнеса".
{% endswagger-parameter %}

{% swagger-parameter in="body" name="script_id" type="integer" %}
ID скрипта (сценария диалога) для запуска, например, 1
{% endswagger-parameter %}

{% swagger-parameter in="body" name="trigger_id" type="integer" %}
ID триггера для запуска, например, 1
{% endswagger-parameter %}

{% swagger-parameter in="body" name="broadcast_id" type="integer" %}
ID рассылки для запуска, например, 1
{% endswagger-parameter %}

{% swagger-parameter in="body" name="script_code" type="string" %}
Кодовое имя сценария диалога для запуска, например, "script_short_code"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="trigger_code" type="string" %}
Кодовое имя триггера для запуска, например, "script_short_code"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="broadcast_code" type="string" %}
Кодовое имя рассылки для запуска, например, "broadcast_short_code"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lead_id" type="integer" %}
ID лида/пользователя для которого выполняем работу, например, 135
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ticket_id" type="integer" %}
ID тикета/таблицы в модели данных для которой выполняем работу, например, 7
{% endswagger-parameter %}

{% swagger-parameter in="body" name="run_at" type="string" %}
Время выполнения в формате "ГГГГ-ММ-ДД чч:мм:сс", например,  "2021-01-21 21:00:00"
{% endswagger-parameter %}

{% swagger-parameter in="body" name="run_after_sec" type="integer" %}
Отсрочка выполнения в секундах, например, 300
{% endswagger-parameter %}

{% swagger-parameter in="body" name="is_periodic" type="boolean" %}
Необходимо ли повторять работу, например, false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="condition_script_code" type="string" %}
Условие выполнения работы в виде JavaScript кода, например "if (leadId == 135) return true;"

\




\


Работа будет запланирована и выполнена только при условии, что код условия вернет истину (true).
{% endswagger-parameter %}

{% swagger-parameter in="body" name="script_request_params" type="object" %}
JSON-объект с входными параметрами к которым можно обратиться из триггера, скрипта или рассылки, например:

\


{ 

\


  "first_param": 7,

\


  "second_param": {

\


    "any_key": "any_value"

\


  }

\


}
{% endswagger-parameter %}

{% swagger-parameter in="body" name="add_tags" type="string" %}
Список тэгов, которыми необходимо пометить пользователя, например, 'tag1,tag2'
{% endswagger-parameter %}

{% swagger-parameter in="body" name="remove_tags" type="string" %}
Cписок тэгов, которые необходимо удалить у пользователя 'tag1,tag2'
{% endswagger-parameter %}

{% swagger-response status="200" description="Cake successfully retrieved." %}
```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endswagger-response %}

{% swagger-response status="404" description="Could not find a cake matching this query." %}
```
{    "message": "Ain't no cake like that."}
```
{% endswagger-response %}
{% endswagger %}

