---
title: The Liskov Substitution Principle
date: 2018-05-08
tags: ["Maintainability Princplies", "SOLID Principles"]
summary: "Any object implementing an interface must be substitutable with every
other object which also implements that interface."
---

Any object implementing an interface must be substitutable with every other
object which also implements that interface.

## Explaination

You must be able to swap a dependency for a derived class (or another
implementation of the same contract) without affecting the correctness of the
application.

New implementations of the same contract cannot behave in a way that code which
depends upon the existing implementations would not expect. This means:

- Pre-conditions cannot be strengthened
- Post-conditions cannot be weakened
- New exceptions cannot be thrown

This helps to create a more predictable and dependable system. Classes can rely
upon their dependencies to always function as they expect them to.

If you violate this principle then you cannot easily swap dependencies, as doing
so could affect the functionality of the system in unexpected ways.

## Remediation

Classes should be refactored so that they all implement the contract in the same
way.

## Examples

```csharp
class User {
    virtual bool CanAccessPage(string pageName) {
        return false;
    }
}

class SuperUser : User {
    override bool CanAccessPage(string pageName) {
        if (pageName == null) {
            throw new NullExceptionError();
        }

        return false;
    }
}
```

In the above example we're violating this principle, because we are now throwing
a new exception which is not thrown in the base class. Any code which depends
upon the base class would not be expecting such an exception to be thrown and so
could behave in unexpect ways.

## Quotes

> Derived classes must be substitutable for their base classes
^[Robert C. Martin]

> If it looks like a duck, quacks like a duck, but needs batteries then you
probably have the wrong abstraction ^[SOLID Development Principles – In
Motivational Pictures. http://lostechies.com/derickbailey/2009/02/11/solid-development-principles-in-motivational-pictures/]
