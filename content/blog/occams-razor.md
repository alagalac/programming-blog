---
title: Occam's Razor
date: 2018-04-24
tags: ["Maintainability Principles"]
summary: "Always choose the solution with the fewest assumptions."
---

There are an infinite number of ways to design and build any feature or fix any
problem. Pick the solution which makes the fewest assumptions.

## Explaination

What this means is you should select the solution which requires the least
knowledge about the rest of the software, instead of the just going with the
first solution which comes to mind.

Functionality with fewer assumptions is less likely to need to change when other
parts of the software change, making it more resilient. This can lead to fewer
bugs, as every time something has to change there is a chance for bugs to be
introduced.

The functionality will likely be less complex and more self-contained, making it
easier to work with.

## Remediation

Try to minimise dependencies. If you do have dependencies then try and use them
by well defined interfaces. Depend upon abstractions and not concrete
implementations.

## Quotes

> Among competing hypotheses, the hypothesis with the fewest assumptions should
be selected. ^[William Ockham]