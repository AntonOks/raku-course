---
title: Аломорфи
---

{% include menu.html %}

Розгляньте наступну програму. Перед її запуском, чи можете ви сказати, які вхідні значення зламають її і на якому рядку?

```raku
my $input = prompt 'Enter something: ';
my Int $i = $input;
my Str $s = $input;

say $i;
say $s;
```

Тут створено три скалярні змінні. Дві з них, `$i` і `$s`, є типізованими змінними. Це означає, що `$i` може зберігати лише цілі числа, а `$s` може зберігати лише рядки.

Тип повернення `prompt` залежить від введених символів. Якщо вхідний рядок може представляти ціле число, результат буде типу `IntStr`, який є _одночасно_ `Int` і `Str`, і таким чином може бути присвоєний як змінній `Int`, так і змінній `Str`. Отже, якщо ви введете, наприклад, `1234`, програма не зламається.

```
$ raku allomorphs.raku
Enter something: 1234
1234
1234
```

Тип `IntStr` є прикладом так званого _аломорфа_ — типу даних, який поєднує два інші типи. Ось ще кілька прикладів.

Якщо ви введете рядок, який не може бути цілим числом, програма зламається в момент присвоєння `$input` до `$i`:

```
$ raku allomorphs.raku
Enter something: Hello, World!
Type check failed in assignment to $i; expected Int but got Str ("Hello, World!")
  in block <unit> at allomorphs.raku line 2
```

Зверніть увагу, що ви отримаєте помилку навіть якщо вхідний рядок може бути перетворений на число, але не на ціле. Оскільки неможливо зберегти число з плаваючою комою або раціональне число в контейнері для цілих чисел, Raku видасть виняток:

```
$ raku allomorphs.raku
Enter something: 3.14
Type check failed in assignment to $i; expected Int but got RatStr (RatStr.new(3.14, "3....)
  in block <unit> at allomorphs.raku line 2
```

Друге присвоєння, `$s = $input`, ніколи не зламається, оскільки рядок може прийняти будь-який вхід.

🦋 Ви можете знайти вихідний код цієї програми у файлі [allomorphs.raku](https://github.com/ash/raku-course/blob/master/essentials/typed-variables/allomorphs/allomorphs.raku).

{% include nav.html %}