---
title: 'Solution: Function table'
---

{% include menu.html %}

Ця програма, ймовірно, є гарним прикладом використання циклу `loop`. З його допомогою ви можете встановити як межі, так і крок безпосередньо в одиницях, які вам потрібні. Зверніть увагу, що ви можете повернутися до цього завдання пізніше після вивчення _послідовностей_ Raku.

## Код

Ось рішення:

```raku
sub f($x) { $x² }

loop (my $x = -3; $x <= 3; $x += 0.1) {
    say "$x\t{f($x)}";
}
```

🦋 Знайдіть програму у файлі [function-table.raku](https://github.com/ash/raku-course/blob/master/exercises/functions/function-table.raku).

## Вивід

Програма друкує довгий список таблиці x — f(x). Частина цього виводу показана тут:

```console
$ raku exercises/functions/function-table.raku
-3	9
-2.9	8.41
-2.8	7.84

. . .

-0.2	0.04
-0.1	0.01
0	0
0.1	0.01
0.2	0.04

. . .

2.7	7.29
2.8	7.84
2.9	8.41
3	9
```

## Візуалізація

Доцільно візуалізувати вивід за допомогою якоїсь зовнішньої програми, наприклад, Excel або gnuplot.

<img src="../f-graph.png" style="width: 500px; height: auto" />

{% include nav.html %}