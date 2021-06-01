# Project

- NAND is given
- From NAND we will create other 30 different gates

There's a logical order from NAND.

1. Not
2. And
3. Or
4. Xor
5. Mux
6. DMux
7. Not16
8. And16
9. Or16
10. Mux16
11. Or8Way
12. Mux4Way16
13. Mux8Way16
14. DMux4Way
15. DMux8Way

# Interesting gates

## Multiplexors

Three inputs: a, b, sel(ector). If the selector is 1, then output b. If the selector is 0, then output a.

I can create these to create "programmable gates", example "AndMuxOr" is an "And" if sele is 1, else is a "Or".

Pro tip: you can write a multiplexor using only And, Or and Not.

## Demultiplexor
The inverse of a multiplexor: distributes the input to one or other channel.

Two inputs: in and sel, two outputs: a, b. 
If sel is zero, in goes to a.
If sel is one, in goes to b.

Pro tip: you can implement it using only 

## And16

Use buses.

## Mux4Way16

Whuuuut. Ok.

You get four inputs which are 16 bits buses, a two bit selector
and a 16 bit output.

OK not so complicated really.

Pro tip: you can build it using several Mux16, maybe some others as needed.

# Pro tips

- Implement the chips in order
- If you don't implement something, if the file is missing, it will use a defualt implementation.
- You can implement "helper chips", but this is not advised.
- Strive to use as few chip-pars as possible
- Buses are indexed right to left (!!!).
