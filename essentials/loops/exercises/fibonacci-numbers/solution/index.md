---
title: Solution of ’Fibonacci numbers’
---

{% include menu.html %}

Fibonacci numbers are defined by the following algorithm.

1. _F<sub>0</sub>_ = 0, _F<sub>0</sub>_ = 1
2. _F<sub>n</sub>_ = _F<sub>n-1</sub>_ + _F<sub>n-2</sub>_

## Code

The code implements the algorithm literary. It uses a couple of variables to keep the current two Fibonacci numbers, and updates them in a loop. Note that both variables get updates [in a single assignment](/raku-course/essentials/scalar-variables/assigning-a-value/#multiple-assignment). 

```raku
my $F0 = 0;
my $F1 = 1;

say $F0;
for ^19 {
    ($F0, $F1) = $F1, $F0 + $F1;
    say $F0;
}
```

🦋 Find the program in the file [fibonacci-numbers.raku](https://github.com/ash/raku-course/blob/master/exercises/loops/fibonacci-numbers.raku).

## Output

Here is the output of the program that prints 20 first numbers.

```console
$ raku exercises/loops/fibonacci-numbers.raku
0
1
1
2
3
5
8
13
21
34
55
89
144
233
377
610
987
1597
2584
4181
```

## More on this subject

Remember this task as we will return to it in the future to get another interesting solution using Raku _sequences_.

{% include nav.html %}
