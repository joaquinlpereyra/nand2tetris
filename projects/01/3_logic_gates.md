Logic gates
===========

Taking boolean logic to real world hardware.  

Elementary logic gate: a simple chip designed to deliver a very basic, well designed functionality. Example: NAND, AND, OR

Composite logic gate: chips designed to deliver more complex funcionality using elementary logic gates.

Elementary gates  examples
----------------

a ----
        NAND --- out
b ----

functional spec: if(a==1 and b==1) then out=0 else=1

Other functionals gates are AND, OR, NOT.

Composite gates
-----------------

a ---- 
b ---- AND --- out
c ----

You can create this only with ANDs of course.

a ----
        AND --------
b ----              |
                   AND ---- out
                    |
c -------------------

Gate interfaces / implementations
----------------
Gates have abstractions too. No one cares about how the three-way AND is implemented, you just have access to those via the gate.

Circuit implementations
----------------

You can implement these gates using hardwired circuits. I read about this in a very good book which name's I don't remember right now.

----/ ----/ ------ out
     a     b

If you move a, b so they continue the circuit, it will reach "out". This is of course AND.

You can do the same for OR.

|---/ -----|
|   a       ---- out
|---/ -----|
|   b


This part about circuits and stuff won't be in this course as this is part of electrical engineering. Interesting though.
