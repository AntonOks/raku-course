---
title: Exercise ‘Trying IntStr’
---

[Start](/raku-course/) / [Part 1](/raku-course/part1) / [Typed variables](/raku-course/typed-variables) / [Exercises](..)

# Trying IntStr

## Task

Consider the following program. Before running it, can you tell which input values will break it and at which line?

    my $input = prompt 'Enter something: ';
    my Int $i = $input;
    my Str $s = $input;

    say $i;
    say $s;

🦋 You can find the source code in the file [intstr.raku](https://github.com/ash/raku-course/blob/master/exercises/typed-variables/intstr.raku).

## Solution

✅ [See the solution and read the comments](solution)

## Next exercise

| [Converting user input to a number](/raku-course/typed-variables/exercises/input-number) →

## Course navigation

← [Typed variables](/raku-course/typed-variables)| [Code blocks](/raku-course/code-blocks) →
