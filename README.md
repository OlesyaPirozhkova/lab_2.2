# lab_2.2

_Лабораторная работа 2.2 Импорт и использование стандартных модулей Python_

> Выполнила: Пирожкова О.П.

> Группа: АБП-231

**Цели:**

Получить практические навыки импорта и использования
функций, классов и констант из стандартной библиотеки Python для решения
прикладных задач.

**Задачи:**
- Изучить понятие "модуль" в Python и его роль в организации кода.
- Освоить различные способы импорта модулей и их компонентов
(import, from ... import, as).
- Познакомиться с функциональностью нескольких ключевых стандартных
модулей, таких как math, random и datetime.
- Научиться находить необходимую информацию в официальной
документации Python.
- Решить практические задачи, применяя функции из стандартных модулей.


# Задание 1

Используя модуль math, вычислите площадь круга по заданному радиусу:

![task_01_2_01]([https://skrinshoter.ru/s/261025/g3E3YTes.jpg?download=1&name=Скриншот-26-10-2025%2016:57:47.jpg])

```
import math

def circle_area(radius):
    return math.pi*radius**2
try:
    radius_input = input()
    radius = float(radius_input)
    area = circle_area(radius)
    print(f"Площадь круга: {area:.2f}")
except ValueError:
    print("Ошибка: Введено нечисловое значение.")
```

# Задание 2

Используя модуль random, сгенерируйте случайное целое число в заданном диапазоне (включительно):

![task_01_2_01]([https://skrinshoter.ru/s/261025/SOyZdaYJ.jpg?download=1&name=Скриншот-26-10-2025%2017:06:39.jpg])

```
import random

def generate_random_int(min_val, max_val):
    if min_val>max_val:
        raise ValueError("Ошибка: Нижняя граница не может быть больше верхней.")
    return random.randint(min_val, max_val)
try:
    min_input = input()
    max_input = input()
    min_val = int(min_input)
    max_val = int(max_input)
    random_number = generate_random_int(min_val, max_val)
    print(f"Случайное число от {min_val} до {max_val}: {random_number}")
except ValueError:
    print("Ошибка: Нижняя граница не может быть больше верхней.")
```

# Задание 3

Используя модуль datetime, выведите текущую дату и время в формате ГГГГ-ММДД ЧЧ:ММ:СС:

![task_01_2_01]([https://skrinshoter.ru/s/261025/6TdB6rjy.jpg?download=1&name=Скриншот-26-10-2025%2017:04:32.jpg])

```
import datetime

def days_between_dates(date1, date2):
    delta = abs(date1 - date2)
    return delta.days

try:
    date1_str = input()
    date2_str = input()
    date_format = "%Y-%m-%d"
    date_start = datetime.datetime.strptime(date1_str, date_format).date()
    date_end = datetime.datetime.strptime(date2_str, date_format).date()
    days = days_between_dates(date_start, date_end)
    print(f"Количество дней между {date_start} и {date_end}: {days}")
except ValueError:
    print("Ошибка: Некорректный формат даты.")
```


**Вывод:**

В ходе работы были получены практические навыки импорта и применения компонентов стандартной библиотеки Python. Освоены ключевые модули (math, random, datetime) и различные способы импорта для решения прикладных задач.
