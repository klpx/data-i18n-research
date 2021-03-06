data-i18n-research
==================

## Задача

Рассмотрим две модели:

    Country: {
      id: [primary key],
      name: [String]
    }

    City: {
      id: [primary key],
      country_id: [fk to country.id]
      name: [String]
    }
    
Перед нами стоят следующие задачи:
* хранение переводов названия городов и стран;
* моментальное редактирование переводов (без пересборок);
* получение сущнсотей с переведенным названием (с поддержкой пасхальной загрузки);
* сортировка по мультиязычным полям.


## Критерий

Установим следующие критерии для отбора среди полученных решений:
* гибкость:
    * *ввод новых языков*,
    * ввод новых полей;
* красота реализации:
    * очевидность всех дополнительно введенных структур,
    * простота использования в коде;
* скорость доступа:
    * *на чтение*;
    * на запись.

В моем случае самыми важными параметрами являются скорость чтения и легкость ввода нового языка. Но рассматривать будем по все критериям.
