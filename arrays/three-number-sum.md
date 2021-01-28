---
title = "Three Number Sum"
tags = ["arrays"]
difficulty = "medium"
---
# Three Number Sum

Difficulty: medium

Algorithms:
1. 3 Nested for loops.
2. Sort, Nested loops (for, while), converging pointers.

## Brute force
Use three nested for loops on input array, x, y and z.
- x starts at 0, increments by 1 until end.
- y starts at x + 1, increments by 1 until end.
- z starts at x + 2, increments by 1 until end.

Add values found from x, y and z to compare to target value.

Time: O(n^3)

Space: 0(n)


## Optimized
Sort the input array in place.

Use a for loop on the array, x.

Set up converging pointers on the right side of the x index.

Add values found from x and pointers and check against target value.
- if over target value, decrement right pointer.
- if under target value, increment left pointer.

Time: O(n^2)

Space: 0(n)