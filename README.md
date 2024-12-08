# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL: an integer counter that lacks proper overflow handling.  The `buggy_counter.vhdl` file contains a counter that will increment beyond its defined range (0 to 15).  This can lead to unpredictable behavior in simulation and synthesis. The `fixed_counter.vhdl` file shows the corrected code.

## Bug Description
The original counter uses an `integer` type without explicitly handling overflow.  When the counter reaches its maximum value (15), it will wrap around to 0 or an unpredictable value. 

## Solution
The solution involves using a `mod` operation to prevent the counter from exceeding its maximum value.  This ensures the counter wraps around correctly.

## How to reproduce
1. Simulate `buggy_counter.vhdl` using your preferred VHDL simulator.
2. Observe the counter's behavior when it reaches values greater than 15.
3. Simulate `fixed_counter.vhdl` and compare its behavior.
