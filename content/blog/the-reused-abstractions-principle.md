---
title: The Reused Abstractions Principle
date: 2018-10-13
tags: ["Maintainability Principles"]
summary: "Your interfaces should be higher level generalised abstractions."
---

Your interfaces should be higher level generalised abstractions.

A proper abstraction is different from necessarily just writing an interface.
Just because you have an interface for a class, it doesn’t mean that you have a
good abstraction.

The implementation should be defined in terms of the interface, not the
interface defined in terms of the implementation.

## Rationale

When working on an application, you want to be dealing with reusable concepts
and ideas rather than getting distracted with lower level implementation
details.

If you design your contracts and interfaces such that there is only one possible
implementation of them then it's a good indication that your abstractions aren't
very generalised and are probably not reusable models.

## Examples

In the real world when you are driving a car, you don't care that the road was
built by a guy named Jim. Likewise your abstractions in your code should not
depend upon specific implementations.

## In code

```csharp
interface SHA1HashingAlgorithm {
    string GenerateHash(string password);
}
```

The above interface is not a good abstraction as it has only one logical
implementation.

```csharp
interface HashingAlgorithm {
 string GenerateHash(string password);
}
```

The above interface is much more abstract and could have many potential
implementations. This makes it easier to re-use and be reasoned with.