Hardware simulation
=================

## Running HDL code

You can take the HDL code and run it in a _hardware simulation_. The class provides one of those.

Or you can write a test script.

Or you can record the output of the simulator and compare it with a desired output in a _compare file_.

## Debugging through printinging
You can tell a .tst file to output all the states

```
load Xor.hdl
output-file Xor.out
output-list a b out;
set a 0, set b 0, eval, output;
...
```
