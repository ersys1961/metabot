---
description: Обращение к боту из внешних систем
---

# Bot API

### Концепция

Бот представляет из себя независимое приложение со собственной бизнес-логикой, моделью данных и состоянием диалога.

Для того чтобы управлять поведением бота из внешних систем вам необходимо запланировать работу \(job\) с помощью Bot API.

Работа это гибкий механизм, который позволяет реализовать практически любую задачу от самых простых \(например, обновить данные пользователя или отправить пользователю текстовое уведомление\) до более сложных \(например, произвести обработку входящих данных перед их передачей пользователю\).

Гибкость достигается это за счет использования встроенного языка программирования JavaScript и системы триггеров.

Сначала в боте на платформе Metabot вы создаете необходимые шаблон сценария диалога и код обработки входных данных, а затем с помощью Bot API планируете работу, которая принимает входные данные и в нужный вам момент передает их в ранее созданные алгоритмы обработки и шаблон сценария.

Шаблон сценария диалога может содержать любую последовательность команда, которую необходимо отправить конечному пользователю \(или пользователям\) в коммуникационный канал. А алгоритм обработки может содержать любые логику от заполнения данных до обращения к внешним API.

Таким образом работа с API бота из внешних систем представляет обращение к хранимым процедурам бота, которые вы создаете в интерфейсе веб-конструктора.

### Доступ к API

Swagger доступен по адресу: [https://test.metabot.dev/api/docs](https://test.metabot.dev/api/docs)

Чтобы получить доступ, достаточно зарегистрировать любой аккаунт на платформе [https://test.metabot.dev](https://test.metabot.dev) \(это тестовый сервер\) или вы можете воспользоваться демо-аккаунтом demoapi@metabot24.com / demoapi1

Для получения доступа к API вашего продуктивного бота обратитесь в поддержку.

Ниже описан основной метод работы с ботом.

{% api-method method="post" host="https://test.cakes.com" path="/bots/{botId}/jobs/schedule" %}
{% api-method-summary %}
Schedule
{% endapi-method-summary %}

{% api-method-description %}
Основной метод для планирования в боте работы.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="botId" type="number" required=true %}
ID вашего бота
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Ваш токен аутентификации. Настраивается в панели администратора в разделе "Пользователи бизнеса".
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="script\_id" type="integer" required=false %}
ID скрипта \(сценария диалога\) для запуска, например, 1
{% endapi-method-parameter %}

{% api-method-parameter name="trigger\_id" type="integer" required=false %}
ID триггера для запуска, например, 1
{% endapi-method-parameter %}

{% api-method-parameter name="broadcast\_id" type="integer" required=false %}
ID рассылки для запуска, например, 1
{% endapi-method-parameter %}

{% api-method-parameter name="script\_code" type="string" required=false %}
Кодовое имя сценария диалога для запуска, например, "script\_short\_code"
{% endapi-method-parameter %}

{% api-method-parameter name="trigger\_code" type="string" required=false %}
Кодовое имя триггера для запуска, например, "script\_short\_code"
{% endapi-method-parameter %}

{% api-method-parameter name="broadcast\_code" type="string" required=false %}
Кодовое имя рассылки для запуска, например, "broadcast\_short\_code"
{% endapi-method-parameter %}

{% api-method-parameter name="lead\_id" type="integer" required=false %}
ID лида/пользователя для которого выполняем работу, например, 135
{% endapi-method-parameter %}

{% api-method-parameter name="ticket\_id" type="integer" required=false %}
ID тикета/таблицы в модели данных для которой выполняем работу, например, 7
{% endapi-method-parameter %}

{% api-method-parameter name="run\_at" type="string" required=false %}
Время выполнения в формате "ГГГГ-ММ-ДД чч:мм:сс", например,  "2021-01-21 21:00:00"
{% endapi-method-parameter %}

{% api-method-parameter name="run\_after\_sec" type="integer" required=false %}
Отсрочка выполнения в секундах, например, 300
{% endapi-method-parameter %}

{% api-method-parameter name="is\_periodic" type="boolean" required=false %}
Необходимо ли повторять работу, например, false
{% endapi-method-parameter %}

{% api-method-parameter name="condition\_script\_code" type="string" required=false %}
Условие выполнения работы в виде JavaScript кода, например "if \(leadId == 135\) return true;"  
  
Работа будет запланирована и выполнена только при условии, что код условия вернет истину \(true\).
{% endapi-method-parameter %}

{% api-method-parameter name="script\_request\_params" type="object" required=false %}
JSON-объект с входными параметрами к которым можно обратиться из триггера, скрипта или рассылки, например:  
{   
  "first\_param": 7,  
  "second\_param": {  
    "any\_key": "any\_value"  
  }  
}
{% endapi-method-parameter %}

{% api-method-parameter name="add\_tags" type="string" required=false %}
Список тэгов, которыми необходимо пометить пользователя, например, 'tag1,tag2'
{% endapi-method-parameter %}

{% api-method-parameter name="remove\_tags" type="string" required=false %}
Cписок тэгов, которые необходимо удалить у пользователя 'tag1,tag2'
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



