# Bloom Festival Prediction

In the hidden Valley of Eldoria, the ancient Aethel Tree is the center of a famous tradition: The Bloom Festival. This festival is held only when the tree blooms, an event which follows a mysterious and ancient pattern.

As the new Village Chronicler, you must study the old records to predict whether the festival will happen in any given year `Y`.

The archives reveal three key observations made by past chroniclers:

- The Regular Cycle: The Aethel Tree blooms every four years. Earliest records show a bloom in year 4, 8, 12, and so on.
- The Century Anomaly: The tree fails to bloom in every "turn-of-the-century" year, e.g., 1700, 1800, 1900 and so on.
- The Great Bloom: On century years like 1200, 1600, 2000, the tree blooms, overriding the anomaly.

Your task is to write a program which, given a year `Y`, predicts whether the Aethel Tree will bloom.

## Input Format

A single line containing one integer, `Y`, representing the year.

## Constraints

- `1 <= Y <= 5000`

## Output Format

Print `FESTIVAL` if the tree will bloom in year `Y`.

Print `NO FESTIVAL` if it will not.

## Sample Input 1

```
2024
```

## Sample Output 1

```
FESTIVAL
```
