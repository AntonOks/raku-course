---
title: Quiz — Ограничения на типовете
---

{% include menu.html %}

Изберете позволените присвоявания в Raku.

{:.quiz}
1 | my Int $a = π.Int;
0 | my Int $b = π; | `π` е `Num`, така че не може да бъде директно присвоен на `Int`.
0 | my Rat $c = π.Int; | Дори ако `π.Int` е `3` и е от „по-тесен“ тип от `Rat`, не е възможно да се присвои.
1 | my Rat $d = π.Str.Rat; | Двойна конверсия на типове, просто за забавление, няма особен смисъл в това, но е легално.
0 | my Num $e = π.Int;
1 | my Num $f = π.Int.Str.Num;

{% include quiz.html %}

{% include nav.html %}