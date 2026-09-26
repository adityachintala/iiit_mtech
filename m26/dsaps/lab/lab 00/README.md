# Lab 00

| # | Problem (this folder) | Closest match | Notes |
|---|---|---|---|
| 1 | [moo-bar](moo-bar.md) | [LeetCode 412 — Fizz Buzz](https://leetcode.com/problems/fizz-buzz/) | Close analog: same idea, but the divisors are 5 and 7 instead of 3 and 5, the words are Moo/Bar/MooBar, and the input has multiple test cases. Loop 1..N and check the "both" case (i % 35) first, O(N) per test. |
| 2 | [not-a-fibonacci](not-a-fibonacci.md) | [LeetCode 509 — Fibonacci Number](https://leetcode.com/problems/fibonacci-number/) | Identical problem, except N goes up to 40 here instead of 30. Iterate with two rolling values in O(N) time and O(1) space (plain recursion is O(2^N)); no modulo is added. |
| 3 | [triangular-number](triangular-number.md) | [LeetCode 441 — Arranging Coins](https://leetcode.com/problems/arranging-coins/) | Close analog: LeetCode asks for the number of complete rows k with k(k+1)/2 <= n, while this asks whether N is exactly triangular (i.e. N = k(k+1)/2 for some k). Either binary search on k in O(log N) or check that 8N+1 is a perfect square (as in LeetCode 367) in O(1). |
