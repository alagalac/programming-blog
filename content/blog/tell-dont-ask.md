---
title: Tell, don't ask
date: 2018-12-06
tags: ["Maintenance Principles"]
summary: "In good object oriented code, data should be bundled in the same class
with the functions which operate on that data."
---

In good object oriented code, data should be bundled in the same class with the
functions which operate on that data. You should tell objects what to do by
calling their methods. You should not be asking other objects about their data
and acting on it.

## Rationale

By telling the object what to do rather than querying its internal data, we are
reducing the amount of knowledge and the dependency that the calling code has on
the internals of the other class.

You don’t want objects acting upon data which belongs to another object, as this
leads to the tight coupling of classes. Tight coupling can make it hard for
future developers to make changes to the system without having to modify a lot
of diﬀerent code.

## Examples

```csharp
if (!user.AllowedPages.Contains(pageToAccess)) {
    user.IsAccountLocked = true;
}
```

In the above example we are directly accessing the data belonging to the User
object.

In the refactored code below we are instead telling the object what to do.

```csharp
user.CheckIfCanAccessPage(pageToAccess);

class User {
    public void CheckIfCanAccessPage(pageToAccess) {
        if (!this.AllowedPages.Contains(pageToAccess)) {
            this.IsAccountLocked = true;
        }
    }
}
```