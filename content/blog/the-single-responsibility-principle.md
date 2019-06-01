---
title: The Single Responsibility Principle
date: 2018-04-25
tags: ["Maintainability Princplies", "SOLID Principles"]
summary: "All objects should have a clear and singular reason to exist, and
hence a clear and singular reason to change (be rewritten)."
---

All objects should have a clear and singular reason to exist, and hence a clear
and singular reason to change (be rewritten).

## Explaination

If summing up what the class does includes the word ”and”, or class would be
challenging for new team members to read and quickly ”get it”, or class has
fields that are only used in some methods, then it violates this principle.

Having a single responsibility helps to keep classes clear and concise. This
results in more readable, understandable and therefore maintainable classes.

Otherwise 'God' classes can start to form. These huge classes can be very
dfficult to maintain and unit test. Sometimes they can grow to be tens of
thousands of lines long.

## Remediation

Try and split large multifunctional classes into smaller classes of discrete
functionality.

![srp1](/img/srp1.png)

In the above diagram you can see a large class with multiple items of fairly
discrete functionality.

![srp2](/img/srp2.png)

The class has been broken up so that the separate items of functionality have
been extracted into their own classes.

## Examples

```csharp
class CredentialsGenerator {
    string GenerateUsername() {
        \\ Username generation functionality
    }

    string GeneratePassword(){
        \\ Password generation functionality
    }
}
```

Could be refactored to

```csharp
class UsernameGenerator {
    string GenerateUsername() {
        \\ Username generation functionality
    }
}
class PasswordGenerator {
    string GeneratePassword(){
        \\ Password generation functionality
    }
}
```

## Quotes

> A class should have only one reason to change. ^[Robert C. Martin]

> Do not try to do everything. Do one thing well. ^[Steve Jobs]