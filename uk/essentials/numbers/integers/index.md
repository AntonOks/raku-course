---
title: Цілі числа в Raku
---

{% include menu.html %}

Тип даних `Int` представляє цілі числа. Числа можуть бути додатними і від'ємними, і ви можете використовувати явний знак `+`, якщо хочете. Ось кілька очевидних прикладів:

```raku
42
-42
100
-5
0
```

Так, звичайний `0` за замовчуванням вважається цілим числом.

## Групи цифр

Raku має цікаву функцію, яка дозволяє писати великі числа з деякими візуальними допоміжними засобами, що розділяють цифри на групи тисяч:

```raku
1_000_000
-3_141_592
```

Хоча ви можете створити число, таке як `34_56`, краще уникати цього, оскільки це може збити з пантелику інших людей, які читають ваш код. Але ви не можете мати два суміжні підкреслення, а також не можете починати або закінчувати число з підкресленням.

## Довільно довгі цілі числа

Raku прекрасно обробляє числа, що виходять за межі 32- або 64-бітних обмежень. Наприклад, наступна програма є прийнятною програмою, яка множить два великі цілі числа і виводить правильний результат.

```raku
say 1_234_456_789_012_345_678_901 * 987_654_321_098_765_432_100;
```

{% include nav.html %}