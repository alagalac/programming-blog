---
title: The Open/Closed Principle
date: 2018-04-27
tags: ["Maintainability Princplies", "SOLID Principles"]
summary: "An object should be open for extension, but closed for modification."
---

An object should be open for extension, but closed for modification.

Once it has been written, there should be no need to ever modify a class unless
fixing a bug.

## Explaination

If the existing code is currently working correctly then why change it? Whenever
you modify a class it is an opportunity to introduce bugs.

If you don't modify existing classes then can reduce the amount of testing
required since nothing has changed.

## Remediation

You can use inheritance to extend a class and add new functionality without
changing the underlying class.

Another way to look at this is you can instead depend upon an abstracted
interface, and use polymorphism to swap out different implementations.

![ocp](/img/ocp.png)

In this diagram we're extending the functionality by editing it.

![ocp2](/img/ocp2.png)

In this diagram we're extending the functionality by creating a new class which
inherits from the old one.

## Examples

```csharp
string ApplyHashingAlgorithm(string password, string algorithm) {
    if (algorithm == "SHA1") {
        // SHA1 implementation
    } else if (algorithm == "SHA2") {
        // SHA2 implementation
    }
}
```

In the above example we would need to change this class if we add any new
hashing algorithms.

```csharp
interface HashingAlgorithm {
    string HashPassword(string password);
}

class SHA1 : HashingAlgorithm {
    string HashPassword(string password) {
        // SHA1 implementation
    }
}

class SHA2 : HashingAlgorithm {
    string HashPassword(string password) {
        // SHA2 implementation
    }
}
```

In this example we don't need to change any of the classes for the existing
hashing algorithms if we add a new one.

## Quotes

> You should be able to extend class behaviour, without modifying it.
^[Robert C. Martin]