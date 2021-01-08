---
title: Data type conversion
---

{% include menu.html %}

So far, we have seen a number of data types that Raku supports. Those were different kinds of [numbers](/essentials/numbers) (integers, rational numbers, and floating-point numbers), [strings](/essentials/strings), and [Boolean](/essentials/booleans) type. Each data type has its name in the Raku type system.

`Str` | String of characters
`Int` | Integer number
`Rat` | Rational number
`Num` | Floating-point number
`Bool` | Logical Boolean

There are more data types that Raku understands. We will see them in the further sections of this course.

Raku is a language with the so-called gradual type system. In most cases, you don’t need to worry about specifying the type of the variable. You can reuse the same variable to first store a string and then a number, or convert a number to the string implicitly:

This is a valid program that does not break:

```raku
my $var = 42;
$var = 'string';
```

So is this program:

```raku
my $a = '100';
my $b = 200;
say $a + $b; # 300
```

Nevertheless, Raku allows you to specify the type of things that you can keep in the given variable, if you want to. Also, sometimes you need to convert the values of one type to another type. There are a few ways you can do that.

## Exercises

Please do not skip the exercises after this section as they reveal some additional information about the data types of Raku.

{% include nav.html %}
