# Problem Title: Basketball One-on-One

## Platform : [Kattis](https://open.kattis.com/problems/basketballoneonone)

## Problem Statement
Alice (`A`) and Bob (`B`) are playing basketball one-on-one. The game is represented as a string of alternating `'A'` and `'B'`, where each character indicates who scored the last point. Determine the winner based on the second-to-last character of the input string, as it represents the player with the most points.

## Input
- A single string containing only `'A'` and `'B'`.

## Output
- Print `'A'` if Alice wins, or `'B'` if Bob wins.

## Example
### Input
```
ABA
```

### Output
```
A
```
---

## Solution Approach
The second-to-last character of the input string determines the winner since the game alternates between Alice and Bob. Simply print this character.

### Python
```python
print(input()[-2])
```
