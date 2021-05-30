Boolean Function Synthesis
====================

We know how to get a truth table from a boolean expression. How to do the opposite?

There is an actual algorithm by which you can construct a "disjunctive normal form".

The steps and simple:
1. Go over the rows which results is one.
2. Construct formula for each of those rows.
3. OR the formulas.
4. Optional: Simplify the mess

| x | y | z | f |
|---------------|
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |

Row zero: NOT(x) AND NOT(y) AND NOT(z)
Row two:  NOT(x) AND y AND NOT(z)
row four: x AND NOT(y) AND NOT(z) 

Complete formula: 
(NOT(x) AND NOT(y) AND NOT(z)) OR 
((NOT(x) AND y and NOT (z)) OR
(x AND NOT(y) AND NOT(z))

**Theorem**: Everything boolean can be represented AND, OR and NOT.

**Better theorem**: We can ditch the OR. Proof: (x OR y) = NOT(NOT(x) AND NOT(y))

**Super better theorem**: You can combine AND and NOT, make NAND and do everything. Proof: NOT(x) = (x NAND x); (x AND y) = NOT(x NAND y)
