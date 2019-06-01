---
title: The Interface Segregation Principle
date: 2018-10-08
tags: ["Maintainability Princplies", "SOLID Principles"]
summary: "Objects should implement multiple specific interfaces rather than
large catch-all interfaces."
---

Objects should implement multiple specific interfaces rather than large
catch-all interfaces.

## Explaination

Large catch-all interfaces are problematic.

All implementations will need to implement all methods on the interface. This
may include methods which are not relevant to them. This means that you may have
a lot of unused code, and more work for developers to implement them.

Catch-all interfaces also increase the complexity of an application, as there
are more potential methods on the interface to consider and keep track of.

Finally, such interfaces are less reusable and it is less likely that there are
can be different implementations of them making it more difficult to modify
the behaviour of the application.

## Remediation

Try to see if larger super interfaces can be broken down into a series of
logical smaller interfaces.

## Examples

```csharp
interface IUserService {
    void UpdatePassword(string newpassword):

    void AuthenticateUser(User user);
}
```

Could be refactored to

```csharp
interface IPasswordService {
    void UpdatePassword(string newpassword):
}

interface IAuthenticationService {
    void AuthenticateUser(User user);
}
```