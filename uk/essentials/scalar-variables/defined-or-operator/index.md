---
title: Оператор defined-or
---

{% include menu.html %}

Використовуйте так званий оператор _defined-or_ `//`, щоб отримати резервне значення, якщо змінна ще не встановлена.

```raku
my $a = 'alpha';
say $a // 'gamma';

my $b;
say $b // 'delta';
```

Ця програма виводить:

```
alpha
delta
```

Значення `$a` встановлено в першому рядку, тому в виразі `$a // 'gamma'` використовується поточне значення `$a`. На противагу цьому, змінна `$b` не була ініціалізована, тому `$b // 'delta'` повертає правий операнд, і програма виводить `delta`.

## //=

Комбінація `//` та `=` дає оператор `//=`, який присвоює значення, якщо змінна не визначена.

```raku
my $x;
$x //= 42;
say $x; # 42
```

{% include nav.html %}