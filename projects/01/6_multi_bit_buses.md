Multi bit buses
===============

We manipulate an array of bits together. We think of those arrays
as one entity. These arrays are called "buses".

HDL has some notation to help with this.

```
CHIP Add16 {
    IN a[16], b[16];
    OUT out[16];

    PARTS:
    // now implement it

    // if i needed to get
    // a single bit
    // i can write a[0], a[1]...

    // we can also use subbusses
    // a[0..7]  gets the first 6 bits of the bus a

    // particularities of our hdl
    // overlap of subbuses are allowed on output buses of parts
    // withd of internal pin is deduced
    // "false" and "true" may be used with buses of any width
}
```
