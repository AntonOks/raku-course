---
title: Solution of ’Purchase table‘
---

[Start](/raku-course) / [Part 1](/raku-course/part1) / [Strings](/raku-course/strings) / [Exercises](../..) / [Purchase table](..)

# The solution of ‘Purchase table’

## Code

Here is a possible solution of this task:

    my $chair-price = 20.57;
    my $chairs = 4;
    my $chairs-total = $chair-price * $chairs;

    my $table-price = 50.18;
    my $tables = 1;
    my $tables-total = $table-price * $tables;

    say "Item\tPrice\tN\tTotal";
    say "Chairs\t\$$chair-price\t$chairs\t\$$chairs-total";
    say "Tables\t\$$table-price\t$tables\t\$$tables-total";

All the numbers are hard coded and saved in a number of variables. We are also using multiplication operator `*` to compute the result. We’ll learn more about operators in the next section of this course, but at this point the construction such as `$chair-price * $chairs` should not be something that you cannot understand.

The three lines that generate output print the three lines of the table, including its header. Notice how the columns are separated by the tab characters `\t`. In the data rows, we also see an escaped dollar character: `\$` as well as different variables that we want to interpolate.

🦋 You can find the source code in the file [purchase-table.raku](https://github.com/ash/raku-course/blob/master/strings/exercises/purchase-table/solution/purchase-table.raku).

## Output

Run the program and see how it prints the table:

    $ raku purchase-table.raku
    Item    Price   N      Total
    Chairs  $20.57  4      $82.28
    Tables  $50.18  1      $50.18

## Comments

Did you notice the hyphens in the name of the variables such as `$chair-price` or `$tables-total`? This is an acceptable way of naming variables in Raku. We’ll touch this in one of the later sections soon.

Don’t be confused by the two adjacent dollar symbols. Raku reads them separately. For example, in the substring `\$$price`, the first dollar sign is escaped and thus represents itself, while the second one is a part of the variable name `$price`.

All the strings are quoted in double quotes to allow interpolation of the variables and the special characters.

Let us return to this task again after we get familiar with arrays.

## Next exercise

| [Name length](../../name-length) →

## Course navigation

← [Strings](/raku-course/strings) / [String length](/raku-course/strings/string-length) | [Numbers](/raku-course/numbers) →



