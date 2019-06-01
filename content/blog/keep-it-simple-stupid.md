---
title: Keep It Simple Stupid
date: 2018-04-25
tags: ["Maintainability Principles"]
summary: "When writing software, simplicity beats cleverness every time."
---

When writing software, simplicity beats cleverness every time. Try and make your
software as simple and as easy to understand as possible.

## Explaination

Writing clever software which uses advanced language features to do something
can be satisfying. However such clever software can be difficult to understand
which makes fixing bugs or adding new features difficult.

## Remediation

See if you can refactor complex or clever code so that it is more readily
understandable.

## Examples

```csharp
bool IsPasswordValid(string password) {
    return Regex.IsMatch(password, @"^(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,16}$");
{
```

The above method with a regex is quite clever, but fairly difficult to
understand.

```csharp
bool IsPasswordValid(string password) {
    if (password.length < 8 || password.length > 16) {
        return false;
    } else if (password.Any(char.IsUpper) == false) {
        return false;
    } else if (password.Any(char.IsLower) == false) {
        return false;
    } else if (password.Any(char.IsDigit) == false) {
        return false;
    }

    return true;
}
```

This method is much more verbose, but simpler easier to understand.

## Quotes

> Debugging is twice as hard as writing the code in the first place. Therefore,
if you write the code as cleverly as possible, you are, by definition, not smart
enough to debug it. ^[Brian Kernighan]

> Perfection is reached not when there is nothing left to add, but when there is
nothing left to take away. ^[Antoine de Saint Exupéry]