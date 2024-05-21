---
title: Quiz — Unicode digits and numbers
---

{% include menu.html %}

Спробуйте з'ясувати, які з наступних цифр формують цілі числа, які Raku приймає як значення типу `Int`.

{:.quiz}
1 | 3
1 | 12345
1 | ⓷ | Це вважається числом, а не окремою цифрою.
0 | ⓵⓶⓷⓸⓹ | Тому ви не можете комбінувати їх таким чином, щоб отримати `12345`.
1 | ❷
0 | ❸❹❺
1 | ㊷ | Один символ Unicode під назвою `CIRCLED NUMBER FOURTY TWO`.
0 | ⓸⓶ | Але два числа не є числом.
1 | ㊄ | Окружний китайський 5, і це число `CIRCLED IDEOGRAPH FIVE`.
0 | 五 | Хоча це означає 5, символ не є ні цифрою, ні числом.
0 | 一二三四五

{% include quiz.html %}

## Коментарі

Ви можете взяти наступну програму як відправну точку для гри та дослідження властивостей таких цифр. Розкоментуйте рядки, щоб побачити, чи це компілюється.

```raku
my $x;
$x =  3;
say $x; say $x.WHAT;

$x =  12345;
$x =  ⓷;
# $x =  ⓵⓶⓷⓸⓹;

$x =  ❷;
# $x =  ❸❹❺;

$x =  ⒌;
# $x =  ⒊⒋⒌;

# $x =  ㊀㊁㊂㊃㊄;
$x =  ㊄;
say $x; say $x.WHAT;

# $x =  五;
# $x =  一二三四五;

$x = ㊷;
say $x;
```

🦋 Візьміть код з GitHub: [unicode-digits.raku](https://github.com/ash/raku-course/blob/master/essentials/numbers/integers/quiz2/unicode-digits.raku).

{% include nav.html %}