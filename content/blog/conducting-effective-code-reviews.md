---
title: Conducting effective code reviews
date: 2019-01-05
tags: ["Software Thoughts"]
summary: "Code reviews are an important control in the development process to
ensure that the end code is of a high quality, and to catch bugs early."
---

Code reviews are an important control in the development process to ensure that
the end code is of a high quality, and to catch bugs early. They also help to
spread knowledge around the development team.

## Review yourself first

> Every problem the reviewer identifies in our work should teach us something
new; if it does not, we didn’t do a good enough job checking our work before
submission. ^[Paul Morris]

You should always go over the changes and review them yourself before you put
them up for review. Often you will pick up bugs which you might not have noticed
when you were working on the item. You’re also saving the reviewer’s time as
they don’t have to go through pointing out bugs you could have found yourself.

## Take collective ownership

> Every developer should feel responsible for the entire application developed
by their team. The entire team should be proud of the work accomplished.
^[Francois Zaninotto]

The code solution belongs to everybody. Don't use terms like ”my code” and ”your
code”, the code doesn't belong to individual developers. It is collectively
owned by the team.

## Review the code, not the person

Code reviews aren't about determining whether somebody is a good developer or
not. You're reviewing the code, not the person's abilities. Just because
somebody made a mistake, it isn't necessarily a reflection on their abilities.

Likewise, don’t take it personally if somebody finds bugs in or questions the
architecture of an item which you have been working on. They’re just working to
improve the quality of the shared code.

## Identity a problem, propose a solution

If you can’t identify a problem, then why does the code need to change? If
you’re proposing a change, then you need to be able to explain why the change
should be made. Don’t propose solutions without demonstrating there actually is
a problem. Likewise, if you can’t propose a solution, then how do you know there
is a way to resolve the issue?

Proposing a solution is also an opportunity for the person who created the
review to learn.

## Automate where you can

Static code analysis tools can quickly pick up   certain issues, such as
formatting issues and unit test failures. This saves the reviewer's time and
allows them to focus on more on in depth issues which can't be automatically
detected.

## Keep it positive

Code reviews should be a positive environment designed to improve the quality of
the code. Don't forget to offer praise in reviews too!