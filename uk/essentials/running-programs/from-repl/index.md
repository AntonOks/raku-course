---
title: Запуск з REPL
---

{% include menu.html %}

REPL означає _Read–eval–print loop_ (цикл читання-оцінки-друку). Це вбудований режим оболонки, де ви можете вводити інструкції та отримувати проміжний результат на екрані, включаючи стан змінних та вихідні дані, які генерує ваша програма.

Щоб запустити оболонку Rakudo, просто введіть:

```console
$ raku
Welcome to 𝐑𝐚𝐤𝐮𝐝𝐨™ v2020.10.
Implementing the 𝐑𝐚𝐤𝐮™ programming language v6.d.
Built on MoarVM version 2020.10.

You may want to `zef install Readline` or `zef install Linenoise` or use rlwrap for a line editor

To exit type 'exit' or '^D'
> 
```

Вихід може залежати від поточно встановленої версії компілятора. У наведеному вище виході оболонка рекомендує встановити деякі модулі для кращого користувацького досвіду, тому ви бачите відповідне повідомлення.

В кінці є символ запиту `>`, де ви можете вводити свою програму або її частини. Оболонка буде компілювати її рядок за рядком, як тільки ви натиснете Enter.

    > say 'Hello, World';
    Hello, World
    > 

{% include nav.html %}