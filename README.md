<<<<<<< a764b5ab46e449f22cb7f449ed0272e287e505ef
## USSRHTML
USSRHTML - это компилятор для языка гипертекстовой разметки (ЯГТР), написанный на python.

Компилятор принимает код на языке ЯГТР и выдает файл с кодом на HTML.

ЯГТР - это фантазия на тему того, что было бы, если бы интернет придумали в СССР.
Особенность данного языка - все вводимые команды должны быть доступны на стандартной ЙЦУКЕН клавиатуре, т.е. 
для ввода команд **не нужно переключаться на английскую раскладку**. Кроме того, вместо двойных тегов типа `<body>...</body>` 
используются команды вида `\тело(...)`, что упрощает набор текста.

## Синтаксис ЯГТР

Исходный код файла должен иметь следующую структуру:
```
\голова(...)
\тело(...)
```
Тег `\голова()` является необязательным, `\тело()` - обязательный.
Содержимое документа пишется внутри скобок "\тело(" и ")".

### Служебные символы
Для ввода служебных символов используется символ `\`:
* % - введите `\%`
* \ - введите `\\`
* ( - введите  `\(` (это связано с тем, что символ `(` используется как левая граница команд)
* ) - введите  `\)` (это связано с тем, что символ `)` используется как правая граница команд)


### Команды
`%` - **Комментарий**.  
Комментарий начинается с символа `%` и действует до конца строки

`\пар(...)` - **Параграф**.  
Параграф обозначается с помощью команды `\пар(...какой-то текст...)`

`\ж(...)` - **Полужирный текст**.  
Полужирный текст выделяется с помощью команды `\ж(...какой-то текст...)`

`\к(...)` - **Курсив**.  
Текст выделяется курсивом с помощью команды `\к(...какой-то текст...)`

`\ссылка(...)` - **Ссылка**.  
Команда предназначена для создания ссылок.  `\ссылка::href="адрес_страницы::(текст ссылки)`

`\пдч(...)` - **Подчеркнутый текст**.  
Добавляет подчеркивание к тексту.  `\пдч(...какой-то текст...)`

`\зч(...)` - **Зачеркнутый текст**.  
Отображает текст как перечеркнутый.  `\зч(...какой-то текст...)`

`\под(...)` - **Подстрочный текст**.  
Отображает шрифт в виде нижнего индекса. Текст при этом располагается ниже базовой линии остальных символов строки и уменьшенного размера.  `\под(...какой-то текст...)`

`\над(...)` - **Надстрочный текст**.  
Отображает шрифт в виде верхнего индекса. Шрифт при этом отображается выше базовой линии текста и уменьшенного размера.   `\над(...какой-то текст...)`

### Атрибуты команд
Атрибуты команд можно ввести с помощью конструкции вида:  
`\команда::атрибуты_и_их_значения::(какой-то текст)`

Атрибуты должны быть описаны в синтаксисе html.

Пример:  
`\пар::style="color: green; font-size: 2em"::(Этот текст будет зеленым)`

## Привет, Мир!
Минимальный текст, который может быть скомпилирован, выглядит примерно так:
```
\тело(Привет, Мир!)
```
Выходной файл будет иметь вид:
```
<html>
<body>
Привет, Мир!
</body>
</html>
```

## Запуск
Для запуска из коммандной строки выполните:
```
$python <путь-к-файлу>/HTMLUSSR.py <путь-к-файлу-с-текстом-на-ЯГТР>/<имя-файла>.txt
```
=======
## USSRHTML
USSRHTML - это компилятор для языка гипертекстовой разметки (ЯГТР), написанный на python.

Компилятор принимает код на языке ЯГТР и выдает файл с кодом на HTML.

ЯГТР - это фантазия на тему того, что было бы, если бы интернет придумали в СССР.
Особенность данного языка - все вводимые команды должны быть доступны на стандартной ЙЦУКЕН клавиатуре, т.е. 
для ввода команд **не нужно переключаться на английскую раскладку**. Кроме того, вместо двойных тегов типа `<body>...</body>` 
используются команды вида `\тело(...)`, что упрощает набор текста.

## Синтаксис ЯГТР

Исходный код файла должен иметь следующую структуру:
```
\голова(...)
\тело(...)
```
Тег `\голова()` является необязательным, `\тело()` - обязательный.
Содержимое документа пишется внутри скобок "\тело(" и ")".

### Служебные символы
Для ввода служебных символов используется символ `\`:
* % - введите `\%`
* \ - введите `\\`
* ( - введите  `\(` (это связано с тем, что символ `(` используется как левая граница команд)
* ) - введите  `\)` (это связано с тем, что символ `)` используется как правая граница команд)


### Команды
`%` - **Комментарий**.  
Комментарий начинается с символа `%` и действует до конца строки

`\пар(...)` - **Параграф**.  
Параграф обозначается с помощью команды `\пар(...какой-то текст...)`

`\ж(...)` - **Полужирный текст**.  
Полужирный текст выделяется с помощью команды `\ж(...какой-то текст...)`

`\к(...)` - **Курсив**.  
Текст выделяется курсивом с помощью команды `\к(...какой-то текст...)`

### Атрибуты команд
Атрибуты команд можно ввести с помощью конструкции вида:  
`\команда::атрибуты_и_их_значения::(какой-то текст)`

Атрибуты должны быть описаны в синтаксисе html.

Пример:  
`\пар::style="color: green; font-size: 2em"::(Этот текст будет зеленым)`

## Привет, Мир!
Минимальный текст, который может быть скомпилирован, выглядит примерно так:
```
\тело(Привет, Мир!)
```
Выходной файл будет иметь вид:
```
<html>
<body>
Привет, Мир!
</body>
</html>
```

## Запуск
Для запуска из коммандной строки выполните:
```
$python <путь-к-файлу>/HTMLUSSR.py <путь-к-файлу-с-текстом-на-ЯГТР>/<имя-файла>.txt
```

