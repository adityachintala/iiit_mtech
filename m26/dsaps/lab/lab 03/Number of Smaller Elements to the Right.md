# Number of Smaller Elements to the Right

## Description

You are given an array of integers `arr` of length `n`. For each element
in the array, determine how many elements to its right are strictly
smaller than it.

You must print `n` integers separated by spaces, where the i-th integer
represents the number of smaller elements to the right of arr\[i\].

## Input Format

An integer n --- the size of the array.

A sequence of n integers arr\[0\], arr\[1\], \..., arr\[n-1\]

## Constraints

1 \<= n \<= 10\^5

-10\^9 \<= arr\[i\] \<= 10\^9

## Output Format

Print n space-separated integers, where the i-th integer is the number
of smaller elements to the right of arr\[i\].

## Sample Cases

##### Sample Input 0

**Input:**

    5
    3 4 9 6 1

**Output:**

    1 1 2 1 0

##### Sample Input 1

**Input:**

    4
    5 2 6 1

**Output:**

    2 1 1 0

##### Sample Input 2

**Input:**

    6
    1 2 3 4 5 6

**Output:**

    0 0 0 0 0 0
