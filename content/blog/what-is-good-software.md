---
title: What is good software?
date: 2018-05-22
tags: ["Software Thoughts"]
summary: "Good software is often difficult to describe."
---

Good software is often difficult to describe.

That's not very useful to help us judge whether software is of good quality or
not. We need some criteria against which we can determine whether the the
software we are building is of good quality. This also gives us something that
we can aim for.

Here I'll run through what I think are the main qualities of "good" software.

## Secure

It it of utmost importance that all software is secure. Security is not
optional.

As much as possible any good software should resist attempts by intruders to
perform actions or obtain information which they should not be able to access.

Poor security can cause significant harm to the users of the software.

## Maintainable

Most of software development is maintaining existing software, not writing new
software. So we should bear that in mind when we are developing the software.

We should be aiming to make our software as quickly, cheaply, and easily
maintainable as possible.

Specifically we should focus on the:

- Improving the readability of the code.
- Reducing the complexity of the code.
- Using a consistent coding style.

Computers don't understand code, they understand 1s and 0s. So when we write
code, our audience is other software developers.

## Scalable

Software should perform well with both the current usage, and with expected
future usage. However, try not to over-engineer it.
[You aren't going to need it.](/you-aren-t-going-to-need-it/)

## Testable

Having software which works correctly is important. However, what is more
important is being able to prove that the software is working correctly.

Being testable can mean that the processes are easily isolated and tested
independently of the rest of the system. It can also mean that some of the
testing is automated using practices such as unit testing.

While 100% automated test coverage is a laudable goal, in practice it isn't
always achievable.

## Flexible

The only thing which is certain is that requirements will change. We need to
design our software such that it is flexible and open to extension.

We should be able to change the software without requiring too much work, and
with minimal risk of causing regression issues.