# Find Number of Good Pairs

You are given two arrays of integers `A` and `B`, both of length `N`, and two integers `C` and `D`.

A pair of indices `(i, j)` is called a **good pair** if

`1 <= i < j <= N`

and

`A[i] - A[j] + C <= B[i] - B[j] + D`.

Your task is to find the total number of good pairs.

## Input Format

The first line contains three integers `N C D`, where:

- `N` is the length of the arrays.
- `C` and `D` are integers used in the condition.

The second line contains `N` integers `A[1], A[2], ..., A[N]` representing array `A`.

The third line contains `N` integers `B[1], B[2], ..., B[N]` representing array `B`.

## Constraints

- `1 <= N <= 2 * 10^5`
- `-10^9 <= A[i], B[i], C, D <= 10^9`

The answer may be as large as `N * (N - 1) / 2`, so **use a 64-bit integer type to store the answer.**

## Output Format

Print a single integer — the number of good pairs `(i, j)`.

## Sample Input 1

```
5 3 5
4 2 7 1 6
3 5 2 4 1
```

## Sample Output 1

```
7
```

## Explanation 1

For the first test case, `A = [4, 2, 7, 1, 6]`, `B = [3, 5, 2, 4, 1]` and `C = 3`, `D = 5`.

We check all pairs `(i, j)` where `i < j`. The good pairs are:

- `(1, 3)`: 4 - 7 + 3 = 0 <= 3 - 2 + 5 = 6
- `(1, 5)`: 4 - 6 + 3 = 1 <= 3 - 1 + 5 = 7
- `(2, 3)`: 2 - 7 + 3 = -2 <= 5 - 2 + 5 = 8
- `(2, 4)`: 2 - 1 + 3 = 4 <= 5 - 4 + 5 = 6
- `(2, 5)`: 2 - 6 + 3 = -1 <= 5 - 1 + 5 = 9
- `(3, 5)`: 7 - 6 + 3 = 4 <= 2 - 1 + 5 = 6
- `(4, 5)`: 1 - 6 + 3 = -2 <= 4 - 1 + 5 = 8

Therefore, there are 7 good pairs.

## Sample Input 2

```
4 2 1
1 5 3 7
2 4 6 3
```

## Sample Output 2

```
4
```

## Explanation 2

For the second test case, `A = [1, 5, 3, 7]`, `B = [2, 4, 6, 3]` and `C = 2`, `D = 1`.

The good pairs are:

- `(1, 2)`: 1 - 5 + 2 = -2 <= 2 - 4 + 1 = -1
- `(1, 4)`: 1 - 7 + 2 = -4 <= 2 - 3 + 1 = 0
- `(2, 4)`: 5 - 7 + 2 = 0 <= 4 - 3 + 1 = 2
- `(3, 4)`: 3 - 7 + 2 = -2 <= 6 - 3 + 1 = 4

Thus, there are 4 good pairs.
