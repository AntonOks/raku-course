---
title: Алломорфы
---

{% include menu.html %}

Рассмотрим следующую программу. Можете ли вы сказать, какие входные значения её сломают и на какой строке, до того как запустите её?

```raku
my $input = prompt 'Enter something: ';
my Int $i = $input;
my Str $s = $input;

say $i;
say $s;
```

Здесь создаются три скалярные переменные. Две из них, `$i` и `$s`, являются типизированными переменными. Это означает, что `$i` может хранить только целые числа, а `$s` может хранить только строки.

Возвращаемый тип `prompt` зависит от введённых символов. Если входная строка может представлять целое число, результат будет типа `IntStr`, который является _как_ `Int`, так и `Str`, и, следовательно, может быть присвоен как переменной типа `Int`, так и переменной типа `Str`. Таким образом, если вы введёте, например, `1234`, программа не сломается.

```
$ raku allomorphs.raku
Enter something: 1234
1234
1234
```

Тип `IntStr` является примером так называемого _алломорфа_ — типа данных, который объединяет два других типа. Вот ещё несколько примеров.

Если вы введёте строку, которая не может быть целым числом, программа сломается в момент присвоения `$input` переменной `$i`:

```
$ raku allomorphs.raku
Enter something: Hello, World!
Type check failed in assignment to $i; expected Int but got Str ("Hello, World!")
  in block <unit> at allomorphs.raku line 2
```

Обратите внимание, что вы получите ошибку, даже если входная строка может быть преобразована в число, но не в целое. Поскольку невозможно хранить число с плавающей запятой или рациональное число в контейнере для целых чисел, Raku выдаст исключение:

```
$ raku allomorphs.raku
Enter something: 3.14
Type check failed in assignment to $i; expected Int but got RatStr (RatStr.new(3.14, "3....)
  in block <unit> at allomorphs.raku line 2
```

Второе присвоение, `$s = $input`, никогда не сломается, так как строка может принять любой ввод.

🦋 Исходный код этой программы можно найти в файле [allomorphs.raku](https://github.com/ash/raku-course/blob/master/essentials/typed-variables/allomorphs/allomorphs.raku).

{% include nav.html %}