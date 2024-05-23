---
title: Интроспекция с `WHAT`
---

{% include menu.html %}

Възможно е да се види типът на данните в променлива, като се извика методът `WHAT` върху нея:

```raku
my $n = 42;
my $s = '42';
say $n.WHAT; # (Int)
say $s.WHAT; # (Str)
```

Типът се отпечатва в скоби, както е показано в коментарите. Например, `(Int)` или `(Str)`.

Няма проблем да се извика метод върху самия литерал. Например:

```raku
say 42.WHAT;      # (Int)
say (-1).WHAT;    # (Int)
say 'Hello'.WHAT; # (Str)
say True.WHAT;    # (Bool)
```

Забележете, че в случая с `-1`, поставяме числото в скоби, тъй като `say -1.WHAT` би опитало да негира резултата на `1.WHAT`, което води до изключение.

{% include nav.html %}