---
title = "Smallest Difference"
tags = ["arrays"]
difficulty = "easy"
---

Difficulty: easy

Algorithms:
1. Nested for loop.
2. Sort, While loop with pointers.


## Brute force
Use two nested for loops, one for loop for each array, x and y.
- x and y start at 0, increments by 1 until end.

Subtract values found from x and y and keep track of the smallest difference.

Time: O(n^2)

Space: 0(1)


## Optimized
Sort both arrays in ascending order.

Initialize two variables to use as pointers, i and j = 0.

Use a while loop, with a condition of i less than first arrays length and j less than second arrays length.

Subtract the values from two pointer and store the results if it is the minimum found.

If the value from the i pointer is less than the value from the j pointer then increment i by 1, else increment j by 1.

Time: O(nlogn) + O(mlogm)

Space: 0(1)