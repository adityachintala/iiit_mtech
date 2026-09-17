# Good Subarrays

You are given an array of `n` digits (without leading zeros). A subarray is called **good** if the sum of its digits is equal to the length of the subarray.

More formally, a subarray from index `l` to `r` (1 <= l <= r <= n) is good if:

a[l] + a[l+1] + ... + a[r] = r - l + 1

Your task is to find the number of good subarrays.

## Input Format

The first line contains a single integer `t` — the number of test cases.

Each test case consists of two lines:

- The first line contains a single integer `n`, the length of the array.
- The second line contains a **string of `n` digits** representing the array.

## Constraints

1 <= t <= 1000

1 <= n <= 10^5

Each character of the string is a digit from 0 to 9.

**The sum of n over all test cases does not exceed 10^5.**

## Output Format

For each test case, print a single integer on its own line — the number of good subarrays.

Note that the **answer may be large and need not fit in a 32-bit integer.**

## Sample Input 0

```
3
3
120
5
11111
6
100110
```

## Sample Output 0

```
3
15
4
```

## Explanation 0

**Test case 1:** Array = [1, 2, 0]

- Subarray [1] (index 0 to 0): sum = 1, length = 1
- Subarray [2, 0] (index 1 to 2): sum = 2, length = 2
- Subarray [1, 2, 0] (index 0 to 2): sum = 3, length = 3

