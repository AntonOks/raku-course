---
title: Аломорфи
---

{% include menu.html %}

Разгледайте следната програма. Преди да я стартирате, можете ли да кажете кои входни стойности ще я счупят и на кой ред?

```raku
my $input = prompt 'Enter something: ';
my Int $i = $input;
my Str $s = $input;

say $i;
say $s;
```

Тук са създадени три скаларни променливи. Две от тях, `$i` и `$s`, са типизирани променливи. Това означава, че `$i` може да съхранява само цели числа, а `$s` може да съхранява само низове.

Типът на връщане на `prompt` зависи от въведените символи. Ако входният низ може да представлява цяло число, резултатът ще бъде от тип `IntStr`, който е _едновременно_ `Int` и `Str`, и следователно може да бъде присвоен както на променлива от тип `Int`, така и на променлива от тип `Str`. Така че, ако въведете, например, `1234`, програмата няма да се счупи.

```
$ raku allomorphs.raku
Enter something: 1234
1234
1234
```

Типът `IntStr` е пример за така наречения _аломорф_ — тип данни, който комбинира два други типа. Ето още няколко примера.

Ако въведете низ, който не може да бъде цяло число, програмата ще се счупи в момента, в който присвоим `$input` на `$i`:

```
$ raku allomorphs.raku
Enter something: Hello, World!
Type check failed in assignment to $i; expected Int but got Str ("Hello, World!")
  in block <unit> at allomorphs.raku line 2
```

Забележете, че ще получите грешка дори ако входният низ може да бъде преобразуван в число, но не и в цяло число. Тъй като не е възможно да се съхрани число с плаваща запетая или рационално число в контейнер за цели числа, Raku ще издаде изключение:

```
$ raku allomorphs.raku
Enter something: 3.14
Type check failed in assignment to $i; expected Int but got RatStr (RatStr.new(3.14, "3....)
  in block <unit> at allomorphs.raku line 2
```

Второто присвояване, `$s = $input`, никога няма да се счупи, тъй като низът може да приеме всякакъв вход.

🦋 Можете да намерите изходния код на тази програма във файла [allomorphs.raku](https://github.com/ash/raku-course/blob/master/essentials/typed-variables/allomorphs/allomorphs.raku).

{% include nav.html %}