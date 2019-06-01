---
title: Make your code readable
date: 2018-12-06
tags: ["Readability Principles"]
summary: "Readability is king. As a developer you will spend more time reading
and understanding code than you will writing code."
---

Readability is king. As a developer you will spend more time reading and
understanding code than you will writing code. Therefore you should put in the
effort to ensure that above all else your code as easy to read and understand as
possible for future developers.

Remember that computers only understand binary. If we were writing code just for
computers then we would be programming in binary. Your target audience for the
code you are writing is not the computer which will be running it, but rather
future developers (including yourself).

Here’s a few tips to help you write readable code:

### Consistency is key

It really doesn’t matter what the coding conventions are. Any future reader will
be able to adapt to the conventions of the solution relatively quickly. What
does matter is consistency in the application of those conventions. Having
multiple conventions in a solution is confusing, and makes it harder for people
to parse the code. Static analysis tools such as StyleCop are really useful for
helping to enforce a consistent style.

### Use whitespace

Nobody wants to try and read a huge block of text. Use whitespace such as blank
lines to help space out your code and group it together logically on the page.

### Limit method sizes

Long methods can be hard to read and understand. If a method it longer than
around 100 lines of code then you should strongly consider breaking it down into
smaller and easier to read functions.

### Avoid magic numbers

”Magic numbers” are numbers or strings which suddenly appear in the code with no
context. These can be very confusing to the reader. You should try to always use
named variables or constants instead of magic numbers.

### Choose good names

Naming stuff is hard. Try to use meaningful, expressive names in your code which
give an indication of what a it does or what it is used for. This applies to
everything including variables, methods, classes, and even whole applications.

Try and avoid generic sounding names such as GetData().

### Don’t declare early

You should only declare a variable immediately before you use it. Don’t declare
it at the start of the method as this will mean anybody later reading the code
will have to do a lot of scrolling back and forth.

### Limit line lengths

Long lines of code are hard to read and may even force the reader to scroll
horizontally. As a rule of thumb you should try and limit the length of your
lines of code to 80 characters long if possible. Never write code which forces
future readers to scroll horizontally.

### Limit file lengths

Likewise, long ﬁles can be hard to navigate. Finding anything can take a lot of
scrolling. While vertical scrolling is easier than horizontal scrolling, try and
keep file lengths as small as you can. If a file is growing too long then
consider whether its contents can be broken up into multiple files.

### Comment your code

While there are solid arguments that code should be self-commenting (Readable
enough on its own that comments should never be required), its a good idea to
add in comments to help future readers understand your thought process and any
subtleties in how the code works.
