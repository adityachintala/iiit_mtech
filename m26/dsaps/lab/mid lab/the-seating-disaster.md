# The Seating Disaster

Lini ma'am has sprung another surprise slip test. This was also a surprise for the TAs.

The slip test has four versions of the question paper, printed as Set `a`, Set `b`, Set `c` and Set `d`. The classroom has `n` seats arranged in one long row, and the rule Head TA Abhijith 🐐 keeps shouting from the front of the hall is simple: **no two adjacent seats may receive the same set**.

Unfortunately, one TA named Dhruv 🤡 began distributing papers before this rule was announced. Abhijith stopped Dhruv once he came to know about this, but by that time some seats may already have a paper sitting on them and some seats may still be empty.

The TAs now need to know how much room they have left to work with. Count the number of ways to place papers on the remaining empty seats so that the finished row obeys the rule. Two seatings are different if at least one seat receives a different set. The answer grows quickly, so report it modulo `1000000007`.

## Input Format

The first line contains a single integer `n` — the number of seats in the row.

The second line contains a string `s` of length `n`, consisting only of the characters `a`, `b`, `c`, `d` and `?`. The `i`-th character describes seat `i`: a letter means that seat already holds that set and cannot be changed, and `?` means the seat is still empty.

## Constraints

- `1 <= n <= 5 * 10^4`
- `s` contains only the characters `a`, `b`, `c`, `d`, `?`

## Output Format

Print a single integer — the number of valid seatings, modulo `1000000007`. If no valid seating exists, print `0`.

## Sample Input 1

```
3
a?a
```

## Sample Output 1

```
3
```

## Explanation 1

Seats one and three already hold Set `a`, and the seat between them is empty. It cannot receive Set `a`, since that would clash on both sides at once. Sets `b`, `c` and `d` are all fine, so there are three ways to finish the row.

## Sample Input 2

```
4
????
```

## Sample Output 2

```
108
```

## Explanation 2

The TA had not handed out a single paper before being stopped. The first seat may receive any of the four sets, and every seat after it may receive any set except the one to its left, giving `4 * 3 * 3 * 3 = 108` arrangements. Abhijith would like it on record that he stopped the distribution in time.

## Sample Input 3

```
6
?ab?bc
```

## Sample Output 3

```
9
```

## Explanation 3

Two empty seats, and they are far enough apart that neither constrains the other. Seat one sits to the left of a Set `a`, so it may take `b`, `c` or `d`. Seat four is trapped between two Set `b` papers and must avoid `b` on both sides, leaving `a`, `c` or `d`. Three choices times three choices is nine.

Note that the answer is not determined by the number of empty seats alone — where they sit matters just as much.

## Sample Input 4

```
5
a?bbc
```

## Sample Output 4

```
0
```

## Explanation 4

Seats three and four both already hold Set `b`, and neither paper can be moved. The row is in violation before anyone touches the one empty seat, so there is no valid way to finish it. The TAs have agreed to blame the printer.

## Sample Input 5

```
2
?a
```

## Sample Output 5

```
3
```

## Explanation 5

Seat two already holds Set `a`. The empty seat to its left may take any set except `a`, so there are three ways to finish the row.
