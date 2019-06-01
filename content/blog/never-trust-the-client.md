---
title: Never trust the client
date: 2019-05-21
tags: ["Security Principles"]
summary: "Never trust any input which comes from a source you do not control."
---

Never trust any input which comes from a source you do not control.

## Explaination

Always assume any outside sources have been comprised and that all input coming
from them is malicious until proven otherwise.

This includes clients browsing your site, and third parties who you integrate
with. They could be hacked, corrupted, impersonated, or otherwise compromised.
Therefore it is critical that any and all input received from an outside source
is properly validated before we do anything with it.

## Remediation

Always validate all input recieved from the client.

Specifically you should check:

- That the input is within the range of allowable values.
- That the client is not trying to access data they should not have access to.
- That the client is not supplying fields we are not expecting.

## Example

An example here is Amazon once introduced a service where users could read an
unlimited number of books on their Kindle ebook readers, and the authors were
paid based upon how many pages were read. Amazon measured how many pages were
read based upon the furthest page through the book which the reader visited.

Some authors started gaming the system by hiring people to quickly visit the
ﬁrst and last pages of their books, resulting in the author being paid for all
of the pages in the book being read. Amazon was scammed because they didn’t
check that readers actually did read every single page they were paying out for.