---
title = "Validate Subsequence"
tags = ["arrays"]
difficulty = "easy"
---

A subsequence must be in the same order as the original array.

Difficulty: easy

Algorithms:
1. For loop, with one pointer

## Brute force
Initialize a pointer for the subsequence array, y = 0.

Use a for loops on input array, x.
- x starts at 0, increments by 1 until end.

Once the pointer matches the subsequence array's length; break from the foor loop.

Check if the value from the pointer matches the x index of the input array, if it does increament the pointer by 1.

Once the for loop has finished, check if the pointer is equal to the length of the subsequence. If it is, this is a valid subsequence; if not, it is not a valid subsequence.

Time: O(n)

Space: 0(1)