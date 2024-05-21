---
title: Solution to ’Hello, Interpolation!‘
---

{% include menu.html %}

## Code

Here is a possible solution to this problem:

```raku
my $name = prompt 'What is your name? ';
say "Hello, $name!";
```

🦋 You can find the source code in the file [hello-interpolation.raku](https://github.com/ash/raku-course/blob/master/exercises/strings/hello-interpolation.raku).

## Output

Run the program, and it will enter a mode when it waits for your input. After you type the name and press Enter, the program continues and prints the greeting:

```console
$ raku exercises/strings/hello-concatenation.raku
What is your name? Raku
Hello, Raku!
```

## Comments

Notice that this time, the string is double-quoted. In double quotes, variables are interpolated, so their content is placed in the string.

{% include nav.html %}