---
title: Software Principles
date: 2019-05-22
tags: ["Software Thoughts"]
---

Good software is one of those things where you'll know it when you see it.
However it can be difficult to describe.

That's not very useful to help us judge whether software is of good quality or
not. We need some criteria against which we can determine whether the the
software we are building is of good quality. This also gives us something that
we can aim for.

Here I'll run through what I think are the main qualities of "good" software.

## Security

The most important criteria of any software is that it is secure.

This means that it is not possible for malicious users to harm other users of
the software. This can be either directly by causing a loss to them, or
indirectly by stealing their data.

Principles to ensure your software is secure:

- [Never trust the client]({{<ref "never-trust-the-client.md">}})
- [There is no security through obscurity]({{<ref "there-is-no-security-through-obscurity.md">}})
- The principle of least privilege
- Minimise the attack surface

## Debugability

Is is also important that software is debuggable. The lifecycle of an
application does not end once it is shipped to production. Inevitably there will
be issues, and it is important that it is quick and easy for these to be
resolved.

Principles to ensure your software is debuggable:

- [Record all I/O]({{<ref "record-all-i-o.md">}})
- [Make all processes repeatable]({{<ref "make-all-processes-repeatable.md">}})

## Readability

All code is written once, but read multiple times. So it is important that the
code is written in such a way that it is as easy to read and navigate as
possible.

Principles to ensure your software is readable:

- Delete unused code
- Use consistent formatting
- One idea per file
- [The principle of lease surprise]({{<ref "the-principle-of-least-surprise.md">}})

## Maintainablity

Distinct from being readable, all software must be maintainable. This means that
it is easy to make changes with a minimal amount of work.

The SOLID principles are helpful guidelines for creating maintainable software.
They are as follows:

- [The single responsibility principle]({{<ref "the-single-responsibility-principle.md">}})
- [The open / closed principle]({{<ref "the-open-closed-principle.md">}})
- [The liskov substitution principle]({{<ref "the-liskov-substitution-principle.md">}})
- [The interface segregation principle]({{<ref "the-interface-segregation-principle.md">}})
- [The dependency inversion principle]({{<ref "the-dependency-inversion-principle.md">}})

In addition, the following principles are also useful:

- You aren't going to need it
- Don't repeat yourself
- Keep it simple, stupid
- Occham's razor
- Tell, don't ask

## Performance

Finally all software must be performant. This doesn't necessarily mean that all
software needs to be scalable, however it does need to be able to meet the
user's expectations around timeliness.