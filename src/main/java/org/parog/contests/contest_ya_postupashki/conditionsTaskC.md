### Задача 3 - C. Запрос к таблице

|                        | Все языки |
| ---------------------- | --------- |
| Ограничения по времени | 2 секунды |
| Ограничения памяти     | 512MB     |
Петя пришел на стажировку в Яндекс, и первая его задача была познакомиться с SQL.
У Пети есть табличка, состоящая из N строк и М столбцов, значениями которой являются целые числа. Каждой колонке соответствует уникальное имя — строка из латинских символов.

Пете задан запрос из Q ограничений вида: ColumnNameK qK valK.
qK может принимать два значения:
1. ﻿﻿﻿> — учитывать только те строки, где значения в ColumnNameK строго больше valK:
2. ﻿﻿﻿<— учитывать только те строки, где значения в ColumnNameK строго меньше valK
   Задача Пети заключается в том, чтоб посчитать сумму во всех строках, которые удовлетворяют всем ограничениям. Юный стажер уже написал скрипт и вычислил ответ. Но Петя волнуется, что где-то ошибся, поэтому просит вас перепроверить его вычисления.
#### Формат ввода
На первой строке вводятся 3 числа N, M, Q(1 ≤ N × M ≤ 3 * 10^5, 1 ≤ Q ≤ 10^5) - количество строк, столбцов в таблице и количество ограничений в запросе.

В следующей строке вводятся через пробел М слов, состоящих из латинских маленьких букв — название соответствующей колонки, каждая строка по длине не превосходит L (1 ≤ L ≤ 10)

Далее вводятся N строк, в каждой через пробел М целых чисел aij (-10^9 ≤ aij ≤ 10^9) -
элементы i-ой строки.

Потом вводятся Q строк — ограничения к запросу.
Каждая строка имеет вид ColumnNameK qK valK (qK € (<, >); -10^9 ≤ val ≤ 10^9) — k-oe
ограничение в формате, описанном в условии задачи.

Гарантируется, что ColumnNameK, соответствует имени одной из колонок таблицы.
#### Формат вывода
Выведите единственное значение S — сумму всех чисел в строках, удовлетворяющих всем заданным ограничениям.
Если никакая строка не удовлетворяет всем ограничениям — выведите в ответ 0.
#### Примеры

| Ввод                                                  | Вывод |
| ----------------------------------------------------- | ----- |
| 2 2 3<br>a b<br>1 1<br>2 2<br>a < 3<br>b > 1<br>b < 3 | 4     |

