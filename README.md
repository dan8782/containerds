Реализация библиотеки s21_containers.h

## Основные моменты реализации:

- **Язык программирования:** Реализация выполнена на языке C++ стандарта C++17 с использованием компилятора GCC.

- **Стиль кода:** При написании кода использовался стиль оформления кода, рекомендованный Google.

- **Итераторы:** Итераторы использовались для работы с контейнерами.

- **Классы-шаблоны:** Все классы реализованы как шаблоны (template classes).

- **Тесты:** Проведено полное покрытие методов классов контейнеров тестами с использованием библиотеки GTest.

- **Запрещено копирование STL:** При реализации не копировалась реализация Standard Template Library (STL). Однако, при этом следовалась логика STL в части проверок, управления памятью и поведения в аномальных ситуациях.

## Часть 1: Реализация библиотеки s21_containers.h

В рамках данной части проекта были реализованы следующие классы контейнеров:

- list
- map
- queue
- set
- stack
- vector

Файл `s21_containers.h` представляет собой заголовочный файл, включающий различные заголовочные файлы с реализацией указанных контейнеров.

Также предоставлен `Makefile` для тестирования библиотеки с целями `clean` и `test`. Реализация контейнера `list` выполнена через структуру `list`, а не массив.

## Часть 2: Дополнительно. Реализация библиотеки s21_containersplus.h

Дополнительно к основным контейнерам были реализованы следующие классы контейнеров:

- array
- multiset

Файл `s21_containersplus.h` также представляет собой заголовочный файл, включающий различные заголовочные файлы с реализацией указанных дополнительных контейнеров.

Предоставлен `Makefile` для тестирования этой библиотеки с целями `clean` и `test`.

## Часть 3: Дополнительно. Реализация метода insert_many

Реализованы методы, соответствующие таблице:

- Модификаторы: Определение: Контейнеры:
- iterator insert_many(const_iterator pos, Args&&... args): Вставляет новые элементы в контейнер непосредственно перед позицией `pos`. list, vector
- void insert_many_back(Args&&... args): Добавляет новые элементы в конец контейнера. list, vector, queue
- void insert_many_front(Args&&... args): Добавляет новые элементы в начало контейнера. list, stack
- vector<std::pair<iterator,bool>> insert_many(Args&&... args): Вставляет новые элементы в контейнер. map, set, multiset