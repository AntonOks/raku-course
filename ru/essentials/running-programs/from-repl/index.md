---
title: Запуск из REPL
---

{% include menu.html %}

REPL означает _Read–eval–print loop_ (прочитать-выполнить-вывести-повторить). Это
встроенная командная оболочка, которая позволяет вам писать инструкции и выводить
промежуточные результаты на экран, включая состояние переменных и вывод,
генерируемый вашей программой.

Чтобы запустить командную оболочку Rakudo, просто напишите:

```console
$ raku
Welcome to 𝐑𝐚𝐤𝐮𝐝𝐨™ v2020.10.
Implementing the 𝐑𝐚𝐤𝐮™ programming language v6.d.
Built on MoarVM version 2020.10.

You may want to `zef install Readline` or `zef install Linenoise` or use rlwrap for a line editor

To exit type 'exit' or '^D'
>
```

Вывод может зависеть от установленной версии компилятора. В выводе выше REPL
рекомендует установить некоторые модули для более удобной работы, поэтому вы
видите соответствующее сообщение.

В конце присутствует символ запроса `>`, где вы можете вводить вашу программу
или ее части. REPL скомпилирует все, строчка за строчкой, как только вы нажмете
клавишу Enter.

```console
> say 'Hello, World';
Hello, World
>
```

{% assign human=1 %}
{% include nav.html %}
