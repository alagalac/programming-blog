---
title: Don't Repeat Yourself
date: 2018-04-23
tags: ["Maintainability Principles"]
summary: "In the application there should always be a single source of truth for
how every piece of functionality should work."
---

In the application there should always be a single source of truth for how every
piece of functionality should work. There should be only a single way to carry
out each action.

Duplication is bad.

## Explaination

Duplicated functionality means:

- Extra effort spent creating something which already exists.
- Extra effort updating two different versions of the same functionality every
time they need to change.
- Extra effort fixing bugs because you forgot to update the second version of
the functionality.
- Extra effort figuring out which version is the correct one because you let
them get out of sync.
- Extra effort tearing your hair out when you realise that they are both
incorrect, but in different ways.

## Remediation

If you do come across some duplication, you should see if you can extract the
common functionality and have both instances call that instead.

![dry1](/img/dry1.png)

In the above diagram you can see some duplicated functionality.

![dry2](/img/dry2.png)

The duplicated functionality can be extracted so that it only exists once.

## Examples

```csharp
string GeneratePasswordForNewUser(int length) {
    // Password generation algorithm
}

string GenerateForgottenPassword(int length) {
    // Password generation algorithm
}
```

The above code contains the same password generation algorithm duplicated.

```csharp
string GeneratePasswordForNewUser(int length) {
    return GeneratePassword(length);
}

string GeneratePasswordForReset(int length) {
    return GeneratePassword(length);
}

string GeneratePassword(int length) {
    // Password generation algorithm
}
```

Here we have extracted the duplicated algorithm so that it can be shared by both
methods.

## Quotes

> Every piece of knowledge must have a single, unambiguous, authoritative
representation within a system. ^[The Pragmatic Programmer]