# Longest Increasing Subsequence

Given `n` and an integer array, print the **length of the longest
strictly increasing subsequence (LIS)**.

A **subsequence** is a sequence derived from the array by deleting zero
or more elements **without changing the order** of the remaining
elements.

-   `[2, 5, 7]` is a valid subsequence
-   `[5, 2]` is **not valid** (order changed)
-   A subsequence **does not need to be contiguous\`**Constraints\*\*

`1 <= nums.length <= 2500`

`-10^4 <= nums[i] <= 10^4`

**Input Format**

First line contains `n` and the next line contains `n` space seperated
integers.

**Output Format**

Length of the LIS of the array.

**Sample Input 1**

8

10 9 2 5 3 7 101 18

**Sample Output 1**

4

**Sample Input 2**

7

7 7 7 7 7 7 7

**Sample Output 2**

1
