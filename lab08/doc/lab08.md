**Лабораторна робота №7. Функції**

**1. Вимоги**

**1.1 Розробник**

• Мусий Антон Вадимович;
• студент групи КІТ-121а;
• 21.12.2021.

**1.2 Загальне завдання**

Розробити програми, що вирішують завдання за допомогою функцій.

**1.3 Індивідуальне завдання**

Реалізувати функцію, що визначає, скільки серед заданої послідовності чисел таких пар, у котрих перше число
` `менше наступного, використовуючи функцію з варіативною кількістю елементів.

**2. Опис програми**

**2.1 Функціональне призначення**

Програма визначає показник порядку ряду чисел за допомогою функції із варіативною кількістю елементів
get\_indicator\_of\_order\_in\_sequence(). Результат зберігається у змінній indicator\_of\_order. Демонстрація результату
передбачає покрокове виконання програми.

**2.2 Опис логічної структури програми**

Для визначення показника порядку викликаємо функцію *get\_indicator\_of\_order\_in\_sequence*, яка приймає
параметрами кількість елементів *count\_of\_elements* у ряді чисел та ряд із *count\_of\_elements* чисел. Функція
перевіряє кожен елемент ряду із усіма наступними, якщо елемент менший за один із наступних елементів
локальна змінна функції *indicator\_of\_order* збільшується на один. Після перевірки усіх елементів функція
повертає значення змінної *indicator\_of\_order*.

**Функція визначення показника порядку у ряді чисел**

int get\_indicator\_of\_order\_in\_sequence

*Призначення:* визначає показник порядку ряду чисел

*Схема алгоритму функції* подана на рис. 1.

*Опис роботи*: функція перевіряє кожен елемент ряду із усіма наступними, якщо елемент менший за один із
наступних елементів локальна змінна функції *indicator\_of\_order* збільшується на один. Після перевірки усіх
елементів функція повертає значення змінної *indicator\_of\_order*.

*Повертає функція* показник порядку ряду чисел.

Рисунок 1 — Схема алгоритму функції *get\_indicator\_of\_order\_in\_sequence*

***Основна функція***

int main

*Призначення:* головна функція

*Схема алгоритму функції* подана на рис. 2.

*Опис роботи:* задається кількість елементів у послідовності, визначається показник порядку ряду чисел шляхом
виклику функції *get\_indicator\_of\_order\_in\_sequence*.






*Повертає функція* код повернення програми (0).

Рисунок 2 — Схема алгоритму функції main

***Структура проекту***

└── lab07

├── Doxyfile

├── Makefile

├── doc

│ ├── lab07.md

│ ├── lab07.docx

│ └── lab07.pdf

└── src

└── main.c

**2.3 Важливі фрагменти програми**

**Підключення заголовочного stdarg.h для обробки даних у функції із змінною кількістю елементів.**

#include <stdarg.h>

***Початкові дані. Константи.***

#define COUNT\_OF\_ELEMENTS\_IN\_SEQUENCE 5

***Перевірка на порядок пари чисел***

if (va\_arg(factor, int) < va\_arg(factor, int))

**3. Варіанти використання**

Для демонстрації результатів використовується покрокове виконання програми та інші засоби налагодження
відлагодника gdb. Нижче наводиться послідовність дій запуску програми у режимі відлагодження.

Крок 1 (див. рис. 3). Знаходячись в основній процедурі, досліджуємо стан змінних, в тому числі констант.

int main()

{

#define COUNT\_OF\_ELEMENTS\_IN\_SEQUENCE 5

int indicator\_of\_order = get\_indicator\_of\_order\_in\_sequence(COUNT\_OF\_ELEMENTS\_IN\_SEQUENCE, 4, 1, 6, 3,
2);

Рисунок 3 — значення змінних при запуску програми

Крок 2 (див. рис. 4). Дослідження стану змінних наприкінці виконання функції визначення показника порядку
послідовності чисел.

Рисунок 4 — значення порядку послідовності






**Висновки**

` `При виконанні даної лабораторної роботи було набуто практичного досвіду роботи із функціями та функціями із
варіативною кількістю елементів.
