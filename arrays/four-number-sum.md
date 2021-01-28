---
title = "Four Number Sum"
tags = ["arrays"]
difficulty = "hard"
---
# Four Number Sum

Difficulty: hard

Algorithms:
1. 4 Nested for loops.
2. Nested for loops, inside has two concurrent for loops.

## Brute force
Use four nested for loops on input array, see [Three Number Sum](three-number-sum.md) for similar instructions.

Time: O(n^4)

Space: 0(n)


## Optimized
Use two nested for loops on input array, x and y
- x starts at 1, increments by 1 until end - 1.
  - We start at 1, because the first pass would result in no matches.
- y starts at x + 1, increments by 1 until end.

Find the difference of the target value and the value found from x + y, check if differense is stored in hashmap and append values to the return variable.

Once y reaches end of array, start a new for loop.
- k starts at x - 1, decrease by 1 until beginning.

Find the value from x + k, add to hashmap as key, append [x, y] into the value which will be a nested array.

Time: O(n^2)

Space: 0(n)