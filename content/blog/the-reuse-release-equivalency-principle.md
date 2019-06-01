---
title: The Reuse/Release Equivalency Principle
date: 2018-05-23
tags: ["Maintainability Principles"]
summary: "If you're going to depend upon or reuse a piece of functionality, then
it should be a released library."
---

If you're going to depend upon or reuse a piece of functionality, then it should
be a released library. Equivalently, if you want people to reuse some
functionality you wrote, release it as a package.

## Rationale

Copying and pasting functionality between applications is not great. There is no
mechanism to receive updates if a bug is fixed in it, or if a new feature is
added.

By releasing functionality as a package, it is versioned, has a maintainer
(usually), and there is a centralised source where you can go to for updates and
bug fixes.