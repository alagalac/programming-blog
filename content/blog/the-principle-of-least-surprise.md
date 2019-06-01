---
title: The Principle of Least Surprise
date: 2018-05-04
tags: ["Readability Principles"]
summary: "The functionality of a system should not be surprising. It should be
as mundane as possible."
---

The functionality of a system should not be surprising. It should be as mundane
as possible. It should do exactly what the average developer would expect it to
do, nothing more nothing less.

## Explaination

If a class or method does something different than your understanding of how
such code would normally work then it violates this principle. We do not want to
introduce code which doesn’t conform to the rest of the software.

One of the key considerations when developing software is to think about the
people who will be maintaining it in the future. We want the software to be as
maintainable as possible.

Surprising software is more difficult to maintain, as the maintainers never know
how any part of the software is going yo function, particularly after making
changes.

## Remediation

Make sure that everything is clearly named, and that it follows the established
conventions in the codebase.