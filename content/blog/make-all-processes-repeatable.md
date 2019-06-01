---
title: Make all processes repeatable
date: 2018-10-13
tags: ["Debugability Principles"]
summary: "You should aim to make every process quick and easy to repeat with the
same inputs and state."
---

You should aim to make every process quick and easy to repeat with the same
inputs and state.

## Explaination

It is much quicker and easier to debug an application if you can exactly
replicate and repeat the process.

If a process requires a lot of setup to get it into a desired state before you
can debug it then it makes it much harder to work with.

If you can't exactly reproduce the state that the application was running in,
then it might be impossible to reproduce the problem!

Ensuring processes are repeatable also makes it easier to get the application
back into its normal state again if it does encounter a problem.

This will likely require making the system stateless, or at least minimising the
statefulness as much as possible.

## Examples

Some examples of how you can try to make processes repeatable are:

- Try not to store state in memory, and avoid singleton classes.
- Try and break up long-running processes into smaller discrete processes with
the state stored in the database.
- Try and minimise statefulness as much as possible.
- Simplify the process of re-running processes.