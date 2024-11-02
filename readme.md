# FIAS-Parser2

## Совместимость
Протестировано на Python 3.13. На более старых версиях может не работать из-за аннотации типов.

## Описание
Скрипт для парсинга [ФИАС](https://fias.nalog.ru/). Принимает адрес в формате ФИАС, 
возвращает таблицу с объектами по адресу. 

Что умеет:

- Принимать список адресов из файла tasks.txt
- Принимать адрес введённый в консоль
- Выводить результат в консоль
- Сохранять результат в файл
- Фильтровать вывод в файл или консоль по типу объекта. Можно выводить только квартиры, только помещения или всё подряд

## Использование
Запускать из командной строки, если запустить из IDE работать не будет.

## Структура проекта
 - main.py — Основной модуль для запуска программы, включает функции для инициализации сессии, получения токена, отправки запросов и обработки задач.
 - classes.py — Содержит класс RequestConfig, который управляет конфигурацией и выполнением HTTP-запросов.
 - json_processing.py — Модуль для обработки JSON-ответов. Содержит функции для извлечения информации, фильтрации объектов и преобразования данных в удобные форматы (например, в DataFrame).
 - requests_config.py — Модуль с предопределенными конфигурациями для различных этапов работы с API (например, для начального запроса, получения токена и поиска объектов).
 - common_headers.py — Модуль с общими заголовками для запросов.
 - credentials.py — Модуль данными прокси.


## Использованные библиотеки
 - logging - для логирования
 - typing - для аннотаций типов
 - msvcrt - для перехвата нажатия на клавиатуру
 - requests - для запросов
 - json - для работы с JSON
 - os - для работы с файлами
 - re - для работы с регулярными выражениями
 - difflib - для сравнения строк
 - pandas - для работы с таблицами
 - prettytable - для форматирования таблиц