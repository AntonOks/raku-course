---
title: Вікторина — Передача аргументів
---

{% include menu.html %}

## 1

Є функція з наступним визначенням:

```raku
sub f {
    say 'Function called';
}
```

Виберіть правильні виклики цієї функції.

{:.quiz}
1 | f;
0 | f(&apos;&apos;); | Функція не приймає жодних аргументів, але тут отримано один.
0 | f &apos;&apos;; | Те ж саме, що і вище.
1 | f(); | Це правильно, аргументи не передаються.
0 | f (); | Тут передається один аргумент (порожній список).
0 | f(10);

## 2

Є ще одна функція.

```raku
sub g($x, $y) {
    say "Called g($x, $y)";
}
```

Виберіть правильні виклики цієї функції.

{:.quiz}
1 | g(10, 20);
0 | g 10 20; | Немає коми між аргументами.
0 | g(10); | Занадто мало аргументів: потрібно два, передано один.
1 | g 10, 20; | Дужки не потрібні, якщо це не викликає неоднозначності.
0 | g(10,); | Неправильний синтаксис.
0 | g(,20); | Також неправильний синтаксис.
0 | g(&apos;10, 20&apos;); | Передано один аргумент-рядок.
1 | g(&apos;word&apos;, 20); | Аргументи можуть бути різних типів.
0 | g(10, 20, 30); | Занадто багато аргументів.
0 | g 10, 20, 30; | Те ж саме: передано три аргументи.


{% include quiz.html %}

{% include nav.html %}