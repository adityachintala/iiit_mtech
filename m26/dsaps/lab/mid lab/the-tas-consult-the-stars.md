# The TAs Consult the Stars

After the poor performance of students in the last DSAPS slip test, the **head TA Abhijith 🐐** sat down and thought very hard about what had gone wrong. It was not the questions. It was not the students. It was, obviously, the **timing**.

So the TA consulted an astrologer just outside campus, who — for a modest fee — delivered his verdict: a slip test may only be held on a day that is **harmonious**. Counting days from the start of the semester, day `d` is harmonious if `d` can be built by multiplying together only 2s, 3s and 5s. If any other prime sneaks into its factorisation, the day is cursed and the test is off.

Day 12 is harmonious, since 12 = 2 × 2 × 3. Day 7 is cursed, because 7 is a prime nobody on the faculty trusts. Day 14 is also cursed, since 14 = 2 × 7 and that 7 ruins everything. Day 1 is declared harmonious by decree — the astrologer's fee covered it.

The TAs will hold their slip tests on harmonious days, in order: the first test on the first harmonious day, the second on the second, and so on. The batch would very much like to know how much time it has left.

Given `n`, find the day number on which the n-th slip test will be held.

## Input Format

A single integer `n`, the index of the slip test you are dreading.

## Constraints

- `1 <= n <= 1690`

## Output Format

A single integer: the day number of the n-th harmonious day.

## Sample Input 1

```
10
```

## Sample Output 1

```
12
```

## Explanation 1

Walking through the first twelve days of the semester: days 1, 2, 3, 4, 5 and 6 are all harmonious. Day 7 is cursed by the prime 7. Days 8, 9 and 10 are harmonious again. Day 11 is cursed by the prime 11. Day 12 = 2 × 2 × 3 is harmonious.

That gives the harmonious days in order as 1, 2, 3, 4, 5, 6, 8, 9, 10, 12 — so the 10th slip test lands on **day 12**, and the batch has just under a fortnight to prepare.

## Sample Input 2

```
1
```

## Sample Output 2

```
1
```

## Explanation 2

Day 1 is harmonious by decree, so the very first slip test is held on the first day of the semester. The TAs consider this excellent motivation.
