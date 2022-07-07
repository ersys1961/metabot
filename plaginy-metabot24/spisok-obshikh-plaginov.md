# Список общих плагинов

#### **moment**

&#x20;           Подключается только через _require()_

```
let moment = require('moment');
```

#### **moment-with-locales**

&#x20;           Подключается только через _require()_

```
let moment = require('moment-with-locales');
```

Это OpenSource библиотека для работы с датами, [https://momentjs.com/](https://momentjs.com/)

Версия библиотеки moment.js: 2.29.3

#### &#x20;**Common.Bot.Commands**

&#x20;            Подключается через _requre()_ или через snippet()

```
require('Common.Bot.Commands');
// или
snippet('Common.Bot.Commands');
```

Если для вашей ситуации доступно подключение через _require()_ – то это более предпочтительный с точки зрения производительности вариант, используйте именно его. Если подключение с помощью _require()_ недоступно или не приемлемо, то используйте подключение через _snippet()_.
