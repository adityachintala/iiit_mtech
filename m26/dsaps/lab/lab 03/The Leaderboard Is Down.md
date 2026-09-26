# The Leaderboard Is Down

## Problem Statement

The DSAPS TAs are running a contest in the lab, and it is going about as
well as everything else they organise.

The projector that was supposed to display the live leaderboard died
twenty minutes in. The TAs looked at it, agreed it was definitely
broken, and moved on. So now, whenever the batch gets restless and wants
to know who is winning, someone shouts across the lab and a TA announces
the current leader out loud.

Scores are entered as students finish. Each student solves the problem
set once and has a single score recorded, and that score never changes
afterwards. The leader is whoever currently has the **highest score**.
If several students are tied at the top, the leader is the one whose
name comes **first alphabetically** --- the head TA reads the roll list
in order and simply stops at the first name she finds.

You have been put in charge of announcing the leader, since you are the
only TA who can be trusted with it. You will be given `q` events, each
of one of two types:

-   `SCORE <name> <points>` --- the student `name` has finished, and
    their score of `points` is entered onto the leaderboard.
-   `LEADER` --- the batch wants to know who is winning. Announce the
    name of the current leader. If nobody has finished yet, announce
    `NO SUBMISSIONS` instead, and everyone goes back to arguing about
    the projector.

## Input Format

The first line contains a single integer `q`, the number of events.

Each of the next `q` lines contains one event: the word `SCORE` followed
by a name and an integer, or the single word `LEADER`.

## Output Format

For each `LEADER` event, output a single line containing the name of the
current leader, or `NO SUBMISSIONS` if no scores have been entered yet.

## Constraints

-   `1 ≤ q ≤ 2 × 10⁵`
-   Each name is a non-empty string of at most `20` lowercase English
    letters
-   `0 ≤ points ≤ 100`
-   All names in `SCORE` events are distinct --- each student\'s score
    is entered exactly once

## Sample Input 1

    9
    LEADER
    SCORE kabir 72
    LEADER
    SCORE meera 55
    LEADER
    SCORE rohit 91
    LEADER
    SCORE arjun 91
    LEADER

## Sample Output 1

    NO SUBMISSIONS
    kabir
    kabir
    rohit
    arjun

### Explanation

The first `LEADER` comes before anyone has finished, so there is nothing
to announce and the answer is `NO SUBMISSIONS`.

kabir finishes with 72 and leads by default. meera then scores 55, which
is lower, so kabir keeps the lead.

rohit finishes with 91 and takes over. Finally arjun also scores 91,
tying rohit at the top --- and since `arjun` comes before `rohit`
alphabetically, **arjun** is announced as the leader.

## Sample Input 2

    8
    SCORE vikram 88
    LEADER
    SCORE tara 40
    LEADER
    SCORE zoya 88
    LEADER
    SCORE ananya 90
    LEADER

## Sample Output 2

    vikram
    vikram
    vikram
    ananya

### Explanation

vikram scores 88 and leads.

tara scores 40, which is too low to matter. zoya scores 88 and ties
vikram --- but `vikram` comes before `zoya` alphabetically, so vikram
holds the lead.

ananya then scores 90, beating 88 outright, and is announced as the new
leader.
