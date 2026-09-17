# Network Coverage

A research colony on Kepler-9 has expanded its sensor relay network into the foothills of a single mountain range, and the way the engineers strung the cables left the network shaped like a binary tree: the colony's central dish sits at the top of the range, and every relay station beneath it feeds signal to at most two stations further downhill — one covering the left ridge, one covering the right. A station with no one downhill from it sits at the very edge of the range, exposed to the storms.

A solar storm is inbound, and the colony's engineers need to install **failsafe monitors** before it hits. A monitor bolted onto any relay station can sense the health of exactly three things: **the station immediately uphill** (its parent), **the station itself**, and **the one or two stations immediately downhill** (its children). The rock face blocks any signal beyond that — a monitor cannot see past its immediate neighbors.

A station is considered "safe" if a monitor is bolted to it, to the station immediately uphill from it, or to a station immediately downhill from it.

Monitors are expensive to airlift in, and the colony's chief engineer, Meera, has been told in no uncertain terms that she will get exactly as many as she asks for — and not one more. She needs to know the **minimum number of monitors** required to keep every single relay station safe before the storm arrives.

Given the network, complete the function `minMonitors` in the editor below. It must return the minimum number of monitors needed so that every station in the network is safe.

`minMonitors` has the following parameter:

`TreeNode* root`: the colony's central dish (the root of the relay network)

## Input Format

You are given the root of the relay network directly. Do not read from stdin — input parsing is handled by the locked boilerplate, which builds the tree and passes you its root.

Each node of the tree is a `TreeNode` with an integer `val` (the station's ID, irrelevant to the logic — every station needs the same treatment regardless of its ID) and pointers `left` and `right` to the two stations immediately downhill.

Below is the input format if you want to construct your own custom test case:

- The first line contains a single integer `n`, the number of tokens describing the network.
- The second line contains `n` space-separated integers giving the network in level order, where `-1` denotes no station at that position. The first token is the central dish. For every station present, the next two unconsumed tokens describe the station immediately downhill-left and downhill-right, respectively.
- Trailing `-1` tokens may be omitted. If the token list ends before a station's downhill stations are described, that station has none downhill from it.

## Constraints

- `1 <= n <= 2 * 10^5`
- Every station's ID is `0` (the value never affects the answer)
- The input is guaranteed to describe a valid binary tree in level order.

## Output Format

Return a single integer: the minimum number of monitors required. Print nothing yourself — the boilerplate handles output. If the network is empty, the expected output is `0`.

## Sample Input 0

```
5
0 0 -1 0 0
```

## Sample Output 0

```
1
```

## Explanation 0

The network decodes to:

```
    D1
    /
  D2
  / \
D3   D4
```

A single monitor bolted to D2 senses D1 (uphill), D2 (itself), and D3, D4 (downhill) — every station is safe with just 1 monitor.

## Sample Input 1

```
8
0 0 -1 0 -1 0 -1 0
```

## Sample Output 1

```
2
```

## Explanation 1

The network decodes to:

```
          D1
          /
        D2
        /
      D3
      /
    D4
    /
  D5
```

One monitor cannot cover a chain this deep. Bolting monitors to **D2** and **D4** keeps D1, D2, D3 safe (via D2) and D3, D4, D5 safe (via D4) — every station is safe, with 2 monitors.

