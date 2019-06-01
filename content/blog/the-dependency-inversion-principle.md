---
title: The Dependency Inversion Principle
date: 2018-12-06
tags: ["Maintainability Principles", "SOLID Principles"]
summary: "Objects should depend upon abstractions and not concrete
implementations of their dependencies."
---

Objects should depend upon abstractions and not concrete implementations of
their dependencies.

## Explaination

Traditionally higher level code (such as your business logic) would depend on
lower level code (such as your core framework code). Instead lower level code
should depend upon abstractions which are either owned by the higher level code
or an external module.

Your highler level code is usually your business logic and hence your most
valuable code, and so you want it to be as portable as possible and not to
have too many dependencies.

Another advantage of this approach is that it makes it easier to mock
dependencies to carry out unit testing.

## Remediation

In the following digram, the higher level code in dependent on the lower level
code.

![dip1](/img/dip1.png)

In the following diagram, the higher level code in dependent upon an interface.
The lower level code implements and hence is dependent upon that interface.

![dip2](/img/dip2.png)

## Examples

```csharp
class User {
    void UpdatePassword(string newPassword) {
        Database db = new Database();
        // ...
        db.SaveChanges();
    }
}
```

In the above example our higher-level User class is dependent upon the
lower-level Database class. This should be refactored such that

```csharp
class User {
    private readonly IDatabase _db;

    public User(IDatabase database) {
        _db = database;
    }

    void UpdatePassword(string newPassword) {
        // ...
        _db.SaveChanges();
    }
}

interface IDatabase {
    // ...
}
```

Here we have inverted the dependency such that now the Database class is
dependent on the IDatabase interface in the higher-level code, and the
higher-level User class is now dependent upon the IDatabase interafce rather
than the lower-level Database class.

## Quotes

> Depend on abstractions, not on concretions ^[Robert C. Martin]