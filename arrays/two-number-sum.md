---
title = "Two Number Sum"
tags = ["arrays"]
difficulty = "easy"
---
# Two Number Sum

Difficulty: easy

Algorithms:
1. Nested for loop.
2. Hashmap lookup.
3. Sort, converging pointers.


## Brute force
Use two nested for loops on input array, x and y.
- x starts at 0, increments by 1 until end.
- y starts at x + 1, increments by 1 until end.

Add values found from x and y to compare to target value.

Time: O(n^2)

Space: 0(1)


## Optimized 1
Use a hashmap for O(1) look up.

Use one for loops on supplied array.
- x starts at 0, increments by 1 until end.

Find the difference of the target value and the value found from x, store the difference in the hashmap.

Time: O(n)

Space: 0(n)


## Optimized 2
Sort the input array in place.

Set up converging pointers on the array.

Add both values from the pointers and check against target value.
- if over target value, decrement right pointer.
- if under target value, increment left pointer.

Time: O(nlogn)

Space: 0(1)