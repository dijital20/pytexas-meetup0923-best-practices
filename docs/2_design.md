# Design

## Rule 1: Make it obvious.

If something is obvious, you don't have to tell the user how to use it... it's, well, obvious. This is the best possible
user experience.

## Rule 2: If you can't make it obvious, make it familiar.

If you can't make it obvious, can you adapt a pattern from another well-known library? If so, you can borrow what your
users know about that library to use yours. You simply have to show or tell the user the pattern that you are using
and the customer knows what they need to know to use your library.

* Does your library work with hierarchical paths? Why not make it work like `pathlib.Path`?
* Serialize or deserialize data? Why not make it work like `json` and `pickle`?

This is even more present in the "magic methods" of Python.

* Class represent a collection of things? Implement `__iter__`, `__len__`, and `__getitem__`.

## Rule 3: If you can't make it familiar, make it well documented.

This is the bulk of the rest of this presentation. If code is documentation, then how do we make this the most readable
code that has ever existed. If a user has to go to the documentation, you have already lost a percentage of your users,
so how do we ensure that the percentage that do find what they are looking for as quickly as possible?

## Rune 4: Start at Rule 1, not Rule 3.

With each step from Rule 1, you are in danger of losing a user. Most users that are inconvenienced will not advertise
the fact or asking for help, they will just leave and find something else.
