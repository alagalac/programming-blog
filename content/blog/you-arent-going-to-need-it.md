---
title: You Aren't Going To Need It
date: 2018-04-24
tags: ["Maintenance Principles"]
summary: "You should not work on new functionality before there is a requirement
for it."
---

You should not work on new functionality before there is a requirement for it.

## Rationale

Future requirements are prone to change. There is usually little point in
building something before you have the requirements for it. You will have to
make many assumptions which may turn out to be incorrect requiring re-work. Even
worse it may turn out that the functionality is no longer required at all,
rendering your work obsolete or unnecessary.

In the event that the functionality is required, it's likely you'll have
forgotten parts of how it works. This means you'll need to spend time figuring
out how it all works again.

Usually it's quicker if you just build it from scratch in the future when the
time comes.

## However...

This doesnt mean that you should have no regard for the future. You should write
your code in such a way that you don't preclude the possibility of extending it
in the future. Following [the SOLID principles](/the-solid-principles/) can help
with this.

## Quotes

>Every line of code we don’t write is dollars we didn’t spend, and time on the
calendar we get back for free. ^[Tim Evans-Ariyeh]