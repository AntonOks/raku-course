---
title: Едноредови коментари
---

{% include menu.html %}

Най-простата форма на коментар е едноредовият коментар. Той започва с символа `#` и продължава до края на текущия ред.

```raku
my $name; # Тази променлива се използва за съхранение на името на потребителя
$name = prompt 'Как се казваш? ';
say $name; # Сега виждаме името
```

Обърнете внимание, че sheebang като `#!/usr/bin/env raku` в първия ред на кода също е коментар за Raku, въпреки че може да бъде прочетен и изпълнен от черупката.

{% include nav.html %}