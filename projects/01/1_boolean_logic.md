Boolean Logic
============

Nothing complicated if you have done some prepositional logic before. Truth tables. AND, OR, NOT, etc.

Boolean functions
------------------
f(x,y,z) = (x AND y) OR (NOT(x) AND z)

We can _always_ write down all possible values of a boolean function, because the domain is restricted to zeros and ones. This can be done with a truth table.

The function and the truth table are the same.

Boolean identities
--------------------
* (x AND y) = (y AND x)
* (x OR y) = (y OR x)
* (x AND (y AND z)) = ((x AND y) AND z)
* (x OR (y OR z)) = ((x OR y) OR z)
* (x AND (y OR z)) = ((x and y) OR (x AND z)
* (x OR (y AND z)) = (x OR y) AND (x OR z) 

Note distribute is both for ORs and ANDs.

Morgan Laws:
* NOT(x AND Y) = NOT(x) OR NOT(y)
* NOT(x OR y) = NOT(x) AND NOT(y)

Idempotency:
* x AND x = x

Double negation:
* NOT(NOT(x)) = x




