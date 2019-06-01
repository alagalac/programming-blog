---
title: Record all I/O
date: 2018-04-29
tags: ["Debugability Principles"]
summary: "You should log or record all input and output from the software."
---

You should log or record all input and output from the software.

## Explaination

External integrations are often some of the most important, but most fragile
areas of an application.

Having the inputs and outputs recorded allow for fast debugging without relying
on third parties for evidence or to set up test scenarios. It allows the
developer to thoroughly investigate with the same inputs as when the error
occurred.

Having such logs is also very important for audit purposes.

This can result in the storage of a lot of data, but storage is relatively cheap
and this data is invaluable when there is a critical problem to be resolved.

There might also be a performance impact from logging so much information,
however the value in having the information for debugging purposes usually
outweighs any performance concerns.

## Examples

Some examples of items you should log include:

- all incoming and outgoing API requests and their parameters.
- all page requests and their parameters for a website.
- all reports and extracts which are generated.
- all exceptions along with the stack trace and parameters.