# coffeediz.schema
Набор компонентов 1С-Битрикс для реализации микроразметки по схеме Schema.org


* coffeediz:schema.org.OrganizationAndPlace - Адрес организации/места
* coffeediz:schema.org.ImageObject - Изображение
* coffeediz:schema.org.SoftwareApplication - Программы
* coffeediz:schema.org.Product - Продукт
* coffeediz:breadcrumb (обёртка над bitrix:breadcrumb) - Хлебные крошки
* coffeediz:schema.org.AggregateRating - Рейтинг (*рекомендуется к использовнаию как свойство для других схем!*)
* coffeediz:schema.org.Offer - Предложение (*рекомендуется к использовнаию как свойство для других схем!*)
 
Документация
-------
* [coffeediz:schema.org.OrganizationAndPlace - Адрес организации/места](http://xn--80ahcjeib4ac4d.xn--p1ai/information/about_microcathode_say_a_word_how_to_implement_microcathode_module_coffeediz_schema_on_the_website_u/#OrganizationAndPlace) 
* [coffeediz:breadcrumb (обёртка над bitrix:breadcrumb) - Хлебные крошки](http://xn--80ahcjeib4ac4d.xn--p1ai/information/about_microcathode_say_a_word_how_to_implement_microcathode_module_coffeediz_schema_on_the_website_u/#breadcrumb) 
* [coffeediz:schema.org.AggregateRating - Рейтинг](http://xn--80ahcjeib4ac4d.xn--p1ai/information/microdesmidae_module_coffeediz_schema_for_1c_bitrix_part_2_rating_images_program/#AggregateRating)
* [coffeediz:schema.org.ImageObject - Изображение](http://xn--80ahcjeib4ac4d.xn--p1ai/information/microdesmidae_module_coffeediz_schema_for_1c_bitrix_part_2_rating_images_program/#ImageObject)
* [coffeediz:schema.org.SoftwareApplication - Программы](http://xn--80ahcjeib4ac4d.xn--p1ai/information/microdesmidae_module_coffeediz_schema_for_1c_bitrix_part_2_rating_images_program/#SoftwareApplication)

**Адрес организации/места**
-------
coffeediz:schema.org.OrganizationAndPlace

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)
* example - содержит минимальное оформление для вывода пользователям + микроразметку

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной).

*Поддерживаемые поля:*
* Тип схемы (место, либо организация, а так же все типы мест/организаций по состоянию на 23.10.2015)
* Название
* Краткое описание
* URL сайта
* Логотип (картинка)
* Адрес
* * Почтовый индекс
* * Страна
* * Город
* * Регион
* * Адрес (улица, дом, офис и т.п.)
* Факс
* Телефон (несколько штук)
* E-mail (несколько штук)
* ИНН
* Время работы (только для типов "Бизнес" и "Административное Здание")
* Географические координаты (только для типа "Бизнес")
* Является свойством другого объекта Schema.org
* Полный набор свойств "Ретинг" с передачей массива параметров компоненту coffeediz:schema.org.AggregateRating
* *Скрыть информации от пользователей (микроразметка видна только поисковикам, но не видна простым юзерам)*



**Хлебные крошки**
-------
coffeediz:breadcrumb (обёртка над bitrix:breadcrumb)

*Шаблоны*:
* coffeediz.data-vocabulary.org
* coffeediz.schema.org

*Суть* - coffeediz:breadcrum это обёртка над bitrix:breadcrumb, позволяющая вывродить его скрытно от пользвоателей (чтобы микроразметку видели только поисковые системы). В остальном можно использовать обычный bitrix:breadcrumb с соответсвующими шаблонами.

*Поддерживаемые поля:*
* *Скрыть информации от пользователей (микроразметка видна только поисковикам, но не видна простым юзерам)*

Google рекомендует схему data-vocabulary.org


**Рейтинг**
-------
coffeediz:schema.org.AggregateRating

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)
* example - содержит минимальное оформление для вывода пользователям + микроразметку

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной). **Рекомендуется к использованию не самостоятельно (не валидируется в этом случае Google), а как свойство других схем!**

*Поддерживаемые поля:*
* *Скрыть информации от пользователей (микроразметка видна только поисковикам, но не видна простым юзерам)*
* "Значение рейтинга" (обязательное)
* "Количество голосов"
* "Количество отзывов"
* "Максимальное значение рейтинга"
* "Минимальное значение рейтинга"
* "Является свойством другого объекта Schema.org"
* "Объект рейтингования" (*пока поддерживает только 1 тип - Место/Организация, НЕ РЕКОМЕНДУЕТСЯ к использованию, поддерживает только БАЗОВЫЕ свойства типа*)


**Изображение**
-------
coffeediz:schema.org.ImageObject

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной).

*Поддерживаемые поля:*
* *Скрыть информации от пользователей (микроразметка видна только поисковикам, но не видна простым юзерам)*
* "Ссылка на изображение"
* "Название картинки"
* "Подпись к картинке"
* "Описание изображения"
* "Высота изображения (px)"
* "Ширина изображения (px)"
* "Ссылка на миниатюру"
* "Является миниатюрой"
* "Изображение описывает контент страницы"
* Полный набор свойств "Ретинг" с передачей массива параметров компоненту coffeediz:schema.org.AggregateRating


**Программы**
-------
coffeediz:schema.org.SoftwareApplication

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной).

*Поддерживаемые поля:*
* *НЕ отображать на сайте (микроразметка видна только поисковикам, но не видна простым юзерам)*
* Тип ПО
* Название
* Краткое и содержательное описание программного продукта (*ОБЯЗАТЕЛЬНОЕ для валидации Яндексом*)
* Категория программы (*Желательное для валидации Google*)
* Подкатегория программы
* Размер и Единица измерения размера дистрибутива
* Количество скачиваний
* Операционная система
* Цена и Валюта
* Полный набор свойств "Ретинг" с передачей массива параметров компоненту coffeediz:schema.org.AggregateRating
* <b>Для Мобильных приложений</b> - Особые требования (Сеть, другие приложения и т.п.)
* <b>Для Веб приложений</b> - Требования к Браузеру


**Предложение**
-------
coffeediz:schema.org.Offer

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной).

*Поддерживаемые поля:*
* *НЕ отображать на сайте (микроразметка видна только поисковикам, но не видна простым юзерам)*
* Цена (Использует "." в качестве разделителя елой и дробной частей, принимает числа)
* Валюта (ISO 4217)
* Доступность
* Состояние
* Способ оплаты
* Тип
* Является свойством другого объекта Schema.org

**Продукт**
-------
coffeediz:schema.org.Product

*шаблоны*:
* .default - содержит ТОЛЬКО микроразметку и вывод данных (без оформления)

*Суть* - статическая обёртка, оформляющая в виде микроразметки массив параметров компонента с автопроверкой заполненности обязательных полей (без которых поисковые системы Яндекс и Google считают микроразметку невалидной).

*Поддерживаемые поля:*
* *НЕ отображать на сайте (микроразметка видна только поисковикам, но не видна простым юзерам)*
* Название
* Описание
* Полный набор свойств "Предложение" с передачей массива параметров компоненту coffeediz:schema.org.Offer
* Полный набор свойств "Ретинг" с передачей массива параметров компоненту coffeediz:schema.org.AggregateRating
* 


Структура репозитория:
-------
* master - модуль в Win-1251 кодирвоке (может использоваться в качестве субмодуля для реальной системы)
* utf8 - модуль в UTF-8 кодировке  (может использоваться в качестве субмодуля для реальной системы)
* distr - набор дистрибутивов для загрузки в Маркетплейс 1С-Битрикс



License
-------
Решение распространяется под лицензией **CC Attribution-ShareAlike (CC-BY-SA)** - http://creativecommons.org/licenses/by-sa/3.0/deed.ru

*Использование решения возможно как частными, так и юридическими лицами для собственных и коммерческих целей, включая полное изменение решения при условии указания авторства решения Задойного А.В. и ссылки [кофедизайн.рф](http://xn--80ahcjeib4ac4d.xn--p1ai/)*
