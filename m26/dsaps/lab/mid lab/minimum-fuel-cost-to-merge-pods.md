# Minimum Fuel Cost to Merge Pods

Given an integer array `resources` of length `n`, representing the resource amounts in pods arranged in a row, and an integer `k`, you need to merge all pods into a single pod by repeatedly combining **exactly `k` consecutive pods** at a time. Each merge operation costs fuel equal to the sum of the resources in the pods being merged, and the resulting pod retains the combined resources. Return the minimum total fuel cost to merge all pods into one, or return `-1` if it is impossible.

## Input Format

- The first line contains two space-separated integers: `n` (the number of resource pods) and `k` (the exact number of consecutive pods to merge in each operation).
- The second line contains `n` space-separated integers representing the `resources` array.

## Constraints

- `1 <= n <= 30`
- `2 <= k <= 30`
- `1 <= resources[i] <= 100`

## Output Format

- Return an integer representing the minimum total fuel cost to merge all pods into one.
- If it is impossible, return `-1`.

## Sample Input 1

```
4 2
3 2 4 1
```

## Sample Output 1

```
20
```

## Explanation 1

- Merge [3,2] to form [5,4,1], costing 5 fuel.
- Merge [4,1] to form [5,5], costing 5 fuel.
- Merge [5,5] to form [10], costing 10 fuel.
- Total cost: 5 + 5 + 10 = 20.

## Sample Input 2

```
4 3
3 2 4 1
```

## Sample Output 2

```
-1
```

## Explanation 2

- After merging [3,2,4] to form [9,1], only two pods remain, but k = 3 requires three pods to merge. Thus, it is impossible to merge into one pod.

## Sample Input 3

```
5 3
3 5 1 2 6
```

## Sample Output 3

```
25
```

## Explanation 3

- Merge [5,1,2] to form [3,8,6], costing 8 fuel.
- Merge [3,8,6] to form [17], costing 17 fuel.
- Total cost: 8 + 17 = 25.
