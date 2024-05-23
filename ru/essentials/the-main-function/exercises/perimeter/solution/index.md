---
title: 'Решение: Периметр прямоугольника'
---

{% include menu.html %}

Эта программа должна уметь принимать один или два аргумента командной строки. В этом решении показан новый трюк. Значение по умолчанию для второй переменной устанавливается равным значению первой переменной: `sub MAIN($a, $b = $a)`. Таким образом, вместо создания двух мультифункций, у нас есть общая функция, которая устанавливает размер второй стороны, если фигура является квадратом.

## Код

Вот решение:

```raku
sub MAIN($a, $b = $a) {
    my $perimeter = 2 * ($a + $b);

    my $shape = $a == $b ?? 'square' !! 'rectangle';
    say "Периметр $shape равен $perimeter.";
}
```

🦋 Найдите программу в файле [perimeter.raku](https://github.com/ash/raku-course/blob/master/exercises/the-main-function/perimeter.raku).

## Вывод

Попробуйте разные входные значения, чтобы протестировать как квадраты, так и прямоугольники.

```console
$ raku exercises/the-main-function/perimeter.raku 1    
Периметр квадрата равен 4.

$ raku exercises/the-main-function/perimeter.raku 1 2
Периметр прямоугольника равен 6.
```

Обратите внимание, что существует третий случай, который также следует протестировать. Если переданы два равных числа, программа должна понять, что это был квадрат:

```console
$ raku exercises/the-main-function/perimeter.raku 2 2
Периметр квадрата равен 8.
```

{% include nav.html %}