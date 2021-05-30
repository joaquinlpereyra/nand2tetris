HDL
=====

How to build our logic gates.

Let's see our XOR gate.

a ---
      XOR --- out
b ---

| x | y | r |
|-----------|
| 0 | 0 | 0 |
| 1 | 1 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |


This has all the information we need to code in HDL. Note
that in this course (i guess only in this course) the inputs
and outputs names are fixed.

```hdl
/ ** XOR gate: out = (a AND NOT(B)) OR (NOT(A) AND (b)) */

CHIP Xor {
    // this part is fixed, can't change the names
    IN a, b;
    OUT out;

    PARTS;
    // Implementation is the only part that I have
    // to be concerned about

    // For this example, we've already built OR, AND and NOT
    // With those gates, we can built the XOR as 
    // described in the topmost comment

    // Next we come up with a gate logic diagram. This part is
    // difficult to write in ASCCI...

    // a --------------------- AND --- |
    //     |                    |      | 
    //     ------ NOT ------    |      |
    //                     |    |      OR --- out
    //     ------ NOT ---- | ---|      |
    //     |               |           |
    // b ----------------- AND  ------ |

    Not (in=a, out=nota);
    Not (in=b, out=notb);

    And (a=a, b=notb, out=aAndNotb);
    And (a=nota, b=b=, out=notaAndb);

    Or (a=aAndNotb, b=notaAndb, out=out); 
}
```

Note that HDL is a declarative language, no for loops no nothing. Because of this, we can write HDL statements in any order. Nevertheless is it customary to write from left to right.

Also note that you need to know and respect the interface of each chip. Not(in=, out=), And(a=, b=, out=), etc.

HDLs
--------------------
* VHDL
* Verilog

And many others.

We use a custom HDL. It is minimal and simpler.

