---
title: Solution of ’Correct the identifiers‘
---

{% include menu.html %}

There are more than one way to make the identifiers correct. Some possible options are shown here:

## Code

    my $AGE = 30;
    my $Name = 'Valdis';
    my $Middle'Name = 'C.';
    my $address2 = 'Second street, 12';
    my $from-to = 'London to Paris';

All the identifiers are valid, but it is probably better to avoid names with apostrophes if you `$don't` have strong reasons to use them.

🦋 You can find the source code in the file [identifiers.raku](https://github.com/ash/raku-course/blob/master/exercises/scalar-variables/identifiers.raku).

## Comments

Let us list the problems with the original names:

* Spaces are not allowed: `$ A G E`.
* A variable needs a sigil: `Name` (it is possible to have sigilles variables in Raku, but they still cannot be declared as `my Name`).
* An apostrophe (a single quote, actually) cannot start a name: `$'Middle'Name`.
* A digit cannot start a name either: `$2address`.
* Two hyphens cannot sit together: `$from--to`.

{% include nav.html %}
