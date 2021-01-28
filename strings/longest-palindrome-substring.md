---
title = "Longest Palindrome Substring"
tags = ["strings"]
difficulty = "medium"
---
# Longest Palindrome Substring

Difficulty: medium

Algorithms:
1. Nested for loop, use O(n) helper function that uses for loop.
2. For loop, use O(n) helper function that uses while loop and pointers.

## Brute force
Create helper function that determines if a string is a palindrone. See [Palindrome Check](palindrome-check.md).

In the main function, initialize a string to hold the longest substring, set initially to an empty string.

Use two nested for loops on input string, x and y.
- x starts at 0, increments by 1 until end.
- y starts at x + 1, increments by 1 until end.

Create a substring by slicing from x to y + 1.

Using a Logical AND, check if the substring is longer than the longest substring and if the substring is a palindrome by using the helper function. If this is true, replace the longest substring with the substring.

Time: O(n^3)

Space: 0(n)


## Optimized
This algorithm will for loop through the string considering each iteration as the middle of the palindrome and use pointers to exapnd outwards;

Create helper function that find the longest palindrone from specific index starting points. This function will have three parameters; the string, a left index, and right index.
- Use while loop, loop while left index >= 0 and right index < string length.
- Check if the values of the indexs on the string don't match; if true break from the while loop, else decreament the left index by 1 and increament the right index by 1.
- Return the resulting substring between the left index and right index.

initialize a string to hold the longest substring, set initially to the ifrst character of the string.
- Note: We initialize with 1 character, because the first iteration will not have a valid left index.

Use for loop on length of input string, x.
- x starts at 1, increments by 1 until end.

Call the helper method for palindromes which have middle a character, we will call this the odd palindrome because it will have an odd length. Left index will be set as x - 1, right index set as x + 1.

Call the helper method for palindromes which do not have a middle character, we will call this the even palindrome because it will have an even length. Left index will be set as x - 1, right index set as x.

Find the longest between the odd and even palindromes, set as current longest substring.

Find the longest between current longest substring and longest substring.

Time: O(n^2)

Space: 0(n)