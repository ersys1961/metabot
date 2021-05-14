# Обращение к внешним системам из бота

Для обращения к внешним сервисам и системам воспользуйтесь шиной интеграций платформы Метабот и встроенным языком программирования JavaScript.

Для демонстрации интеграционных возможностей платформы, приведем пример кода, который загружает валютные курсы с сайта [http://fixer.io](http://fixer.io/) и кэширует их на сутки в базе данных бота.

```text
// Getting preferred rates

var last_updated      = lead.getAttr('last_updated');
var cache             = lead.getJsonAttr('cache');
var today             = Math.floor(Date.now() / 1000);
var rates             = false;
var tmp_rates_message = '';
var token             = 'ваш ключ к сервису';

// Провярем есть ли кэш и не истек ли он (24ч)
if (cache && last_updated*1 > 0 && (today - last_updated < 60*60*24))
{ 
  // Используем кэш
  rates = cache;  
} else {
  // Используем API
  api.setHeaders('{"Accept":"application/json"}');

  // Для отладки
  lead.setJsonAttr("lastHttpResponse", null); 
  lead.setAttr("lastHttpResponseCode", null); 

  // Адрес endpoint
  var url = 'http://data.fixer.io/api/latest?format=1&access_key=' + token;

  // POST запрос
  var jsonResponse = api.postJson(url); 
  var jsonResponseCode = api.getLastResponseCode();

  // Для отладки
  lead.setAttr("lastHttpResponseCode", jsonResponseCode); 
  lead.setJsonAttr("lastHttpResponse", jsonResponse); 

  // В случае успеха
  if (jsonResponseCode == 200) { 
    rates = jsonResponse.rates;
    
    // Кэшируем в лиде
    lead.setAttr('last_updated', today);
    lead.setJsonAttr('cache', rates);
  } 
}

// Формируем текстовое сообщение
if (rates) {
  for(var currency in rates) {
    tmp_rates_message = (tmp_rates_message ? tmp_rates_message + '\n' : '') + 
      currency + ': ' + rates[currency];
  }
}

// Сохраняем в во временную память, доступную только во время текущего сценария
memory.setAttr('tmp_rates_message', tmp_rates_message);
```

