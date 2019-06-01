---
title: Why have principles?
date: 2018-04-21
tags: ["Software Thoughts"]
summary: "What purpose do software principles serve, and why do we have them?"
---

What purpose do software principles serve, and why do we have them?

I think that the main challenge that we face as software developers (besides
scope and deadlines) is the challenge of complexity. By using software
principles, we can try and minimise the complexity of software and maximise the
maintainability.

When writing software it's very easy for the complexity to get get away from
you. To understand how this happens, we need to take a look at the lifecycle of
your average application.

## The lifecycle of an application

Most applications start out as a small, simple, and easy to understand
application. The application will have a clear purpose, and was probably built
by one or two people who know it inside out.

Over time most successful applications evolve, gaining new features. This adds
to the complexity of the application. As applications grow, they may become so
complex that is is impossible for any one person to fully understand all aspects
of it at any one point in time.

The Developers may also leave the team to be replaced by new people. This leads
to a loss of knowledge about the intention of the code and how everything is
supposed to tie together.

These factors can lead to the application being developed with no clear design
goals. New features may be bolted on with little regard to how the integrate
with the existing architecture.

This can quickly lead to what we would call a big
[ball of mud](https://en.wikipedia.org/wiki/Big_ball_of_mud).

## Big ball of mud

A big ball of mud is an application where there is no discernable structure in
the underlying code. Such applications can be difficult and expensive to
maintain.

Usually they are highly complex, but also tightly coupled which makes it nearly
impossible to foresee the affect that a code change may have on the application.
This means that any change may inadvertently introduce a new bug.

## Guided evolution

How do we avoid building such applications then?

Designing applications so that they are easily understandable and maintainable
in the future is hard. It is usually impossible to design an application
upfront. Changing requirements and new features will get in the way of even the
most well-designed architectures.

Instead we need some sensible principles which we can use to guide the evolution
of an application over time so that it is easy to maintain.

That is the reason why software development principles are important, and it is
a good idea to follow them.

## All things in moderation

However, like all things in life these principles should be used in moderation.
At the end of the day the most important thing is delivering working software on
time. Sometimes that means making sacrifices.
