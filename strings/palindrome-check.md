---
title = "Palindrome Check"
tags = ["strings"]
difficulty = "easy"
---
# Palindrome Check

Difficulty: easy

Algorithms:
1. For loop, string concatenation.
2. For loop, array.push.
3. Recursion
4. While loop, pointers

## Brute force
Initialize a string for the creation of the palindrome.

Use for loop on length of input string, x.
- x starts at 0, increments by 1 until end.

Add values found from x and append to palindrome string.

Compare the input and palindrome strings.

Time: O(n^2)

Space: 0(n)


## Brute force 2
Initialize an array for the creation of the palindrome.

Use for loop on length of input string, x.
- x starts at length - 1, decrease by 1 until beginning.

Add values found from x and push to palindrome array.

Compare the input string to the joined palindrome array.

Time: O(n)

Space: 0(n)


## Brute force 3
Use the current function for recurrsion. Have a string parameter and an index parameter i with a default value of 0.

Initialize a second index j with a value of string length - 1 - i.

The stop condition can be performed as a return statement with a ternary condition. When i >= j, check if the values found from i and j match, else call the recursive function with the string and i + 1.

Time: O(n)

Space: 0(n)
- Note: Tail recursion could turn to 0(1)


## Optimized
Initialize two pointers, l and r.
- l starts at 0, this is used as a left side pointer.
- r starts at length - 1, this is used as a right side pointer

Use a while loop, loop while l < r.

Check if the values found from the pointers match, if they don;t then return false. Else increment the l by 1 and decrement the r by 1.

When the while loop finishes, return true.

Time: O(n)

Space: 0(1)