---
description: >-
  Выполнить JavaScript, например, для установки переменных бота или атрибутов
  лида
---

# Выполнить JavaScript

Функциональная команда позволяет выполнить JavaScript, например для установки значений глобальных переменных \(переменных бота\) или атрибутов лида.

Настроить команду _Выполнить JavaScript_ можно, выбрав одноименный пункт **Выполнить JavaScript** из списка **Команд**:

![&#x421;&#x43F;&#x438;&#x441;&#x43E;&#x43A; &#x43A;&#x43E;&#x43C;&#x430;&#x43D;&#x434;](../.gitbook/assets/izobrazhenie%20%28408%29.png)

В диалоговом окне, в поле **JavaScript** необходимо создать, синтаксически верно написанный, JavaScript. 

Нажать кнопку _**Создать**_.

![&#x41D;&#x430;&#x441;&#x442;&#x440;&#x43E;&#x439;&#x43A;&#x430; &#x441;&#x432;&#x43E;&#x439;&#x441;&#x442;&#x432; &#x43A;&#x43E;&#x43C;&#x430;&#x43D;&#x434;&#x44B;](../.gitbook/assets/izobrazhenie%20%28113%29.png)

В редакторе скриптов появляется команда **Выполнить JavaScript**.

![&#x41A;&#x43E;&#x43C;&#x430;&#x43D;&#x434;&#x430; &#x432; &#x440;&#x435;&#x434;&#x430;&#x43A;&#x442;&#x43E;&#x440;&#x435; &#x441;&#x43A;&#x440;&#x438;&#x43F;&#x442;&#x43E;&#x432;](../.gitbook/assets/izobrazhenie%20%28186%29.png)

#### Пример скрипта, для проверки и установки значения переменной бота

```text
//bot.setAttr('globalVarName1', 'var 1 value');
//bot.getAttr('globalVarName1');

bot.setAttr('globalVarName2', bot.getAttr('globalVarName2') + ' Это вторая глобальная переменная');
```

#### Пример скрипта, для проверки и установки значения переменной лида

```text
var currentVar1Value = lead.getAttr('LeadVar1');
var glueStr = 'lead variable value|';
var newValue = glueStr;

//if (lead.isAttrExist('LeadVar1')) {
//   newValue  = currentVar1Value  + glueStr;
//}

if (currentVar1Value  !== null) {
   newValue  = currentVar1Value  + glueStr;
}

lead.setAttr('LeadVar1', newValue);
```



