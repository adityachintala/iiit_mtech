# The Long Walk for DSAPS Slip Test

## Problem Statement

The DSAPS slip test has already started, and you are still in your
hostel room.

Campus is laid out as a neat grid of `m` blocks north to south and `n`
blocks east to west (in simple words a m x n grid). Your room sits at
the north-west corner, block `(1, 1)`. The exam hall sits at the
south-east corner, block `(m, n)`. You are late enough that every second
counts, so you will only ever move **one block east** or **one block
south** --- you can\'t move other directions as you are not on time 😭.

There is one complication. The DSAPS TAs, still nursing a grudge from
your scores from the last slip test, have stationed themselves at
various blocks around campus to catch anyone arriving late. If you walk
into a block where a TA is standing, you will be stopped, lectured about
time management, and the test will be over for you. **Those blocks are
simply not walkable**.

Your friends in the batch are taking bets on how many different routes
you could possibly take. Count the number of distinct routes from your
room to the exam hall that avoid every TA. Since the answer can be
enormous, report it **modulo 1000000007**.

## Input Format

The first line contains two integers `m` and `n`, the number of rows and
columns of the campus grid.

Each of the next `m` lines contains a string of exactly `n` characters
describing one row of campus, from north to south. The character `.`
denotes a clear block, and `#` denotes a block with a TA standing on it.

## Output Format

A single integer: the number of distinct TA-free routes from block
`(1, 1)` to block `(m, n)`, taken modulo 1000000007.

## Constraints

-   `1 <= m, n <= 1000`
-   Each grid character is either `.` or `#`
-   A TA may be standing on your starting block or on the exam hall
    itself, in which case you are simply doomed

## Sample Input 1

    3 7
    .......
    .......
    .......

## Sample Output 1

    28

### Explanation

Campus is completely clear. Every route consists of 2 moves south and 6
moves east in some order, and there are 28 ways to arrange them. You
will take exactly one of these routes and still arrive late.

## Sample Input 2

    3 3
    ...
    .#.
    ...

## Sample Output 2

    2

### Explanation

A single TA is stationed at the centre block, which cuts campus in half
diagonally. Only two routes survive: hug the northern and eastern edge,
or hug the western and southern edge. Both are TA-free, and both are
equally exhausting.

## Sample Input 3

    3 3
    #..
    ...
    ...

## Sample Output 3

    0

### Explanation

A TA is waiting directly outside your room. There are no routes at all,
and there is no point getting out of bed. The answer is 0.
