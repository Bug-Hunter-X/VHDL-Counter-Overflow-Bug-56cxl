# VHDL Counter Overflow Bug

This repository demonstrates a common but subtle bug in VHDL code: integer overflow in a counter.  The `buggy_counter.vhd` file contains a counter that increments on each rising clock edge.  However, it lacks proper handling of the upper bound, leading to an integer overflow when the counter reaches its maximum value.

The solution, provided in `buggy_counter_solution.vhd`, demonstrates how to correctly handle this situation using modulo arithmetic to prevent overflow.

## How to reproduce the bug

1. Synthesize and simulate `buggy_counter.vhd`.
2. Observe the counter's behavior when it reaches the maximum count (15).  The counter may wrap around unexpectedly or display unpredictable behavior.