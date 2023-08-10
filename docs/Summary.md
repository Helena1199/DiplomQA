# Отчёт по итогам автоматизации

## Что запланировано и что сделано

- проведено тестирование веб-сервиса покупки тура "Путешествие дня".
- настроен запуск SUT с подключением к необходимой БД.
- запущена и настроена CI, запускающая тесты на указанных в задании БД: MySQL и PostgreSQL.
- составлен [план автоматизации](https://github.com/Helena1199/Diplom/blob/main/docs/Plan.md) в который входят 88 тестовых сценария (16 сценариев API тестирования и 72 на UI тестирование).
- написан необходимый для автоматизации тестовый фреймворк (
  [page objects](https://github.com/Helena1199/Diplom/blob/main/src/test/java/ru/netology/page/FormPage.java) для взаимодействия с
  элементами веб-сервиса и [Data-helpers](https://github.com/Helena1199/Diplom/tree/main/src/test/java/ru/netology/data) для управления тестовыми данными).
  Большая часть данных в тесте авто-генерируема для избежания эффекта пестицида.
- Все заявленные сценарии автоматизированы
- составлен [отчет](Report.md) по результату прогона тестов.
- заведены 15 [баг-репорта](https://github.com/Helena1199/Diplom/issues) по найденным дефектам.

## Сработавшие риски

- отсутствие технической документации не позволяло четко определить ожидаемый результат в тестах
- требование поддержки двух СУБД (сложные настройки запуска SUT)
- отсутствие у веб-элементов атрибута test-id (сложности с локаторами элементов при составлении page objects).

## Общий итог по времени

|                  | Запланировано, ч  | Потрачено, ч |                                  Обоснование расхождения                                   |
|:-----------------|    :----:   |   :----:   |:------------------------------------------------------------------------------------------:|
| Настройка SUT, создание тестового фреймворка | 10 - 13  | 13 |             -              |
| Создание автотестов  | 10 - 12   | 17 |                         Часть тестов пришлось переписывать                          |
| Создание баг-репортов и отчёта | 5 - 6 | 12 | Дефектов было выявлено больше ожидаемого. Их компоновка и оформление заняло больше времени |  
| Отчёт по результатам автоматизации | 3 | 3 |                                             -                                              |  
| Подключение CI | 5  | 7 |                                             Возникли сложности с установкой headless режима                                              |
| Всего | 33 - 39 | 52 |                                                                                                                                   