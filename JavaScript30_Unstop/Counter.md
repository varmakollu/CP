# Counter Function

## Problem
Given an integer `n`, return a counter function. This counter function initially returns `n` and then returns `1` more than the previous value every subsequent time it is called (`n, n + 1, n + 2, etc`).

| Example | Input                                        | Output                  |
| ------- | -------------------------------------------- | ----------------------- |
| 1       | n = 10  ["call","call","call"]               | [10, 11, 12]            |
| 2       | n = -2  ["call","call","call","call","call"] | [-2, -1, 0, 1, 2]  <br> |


**Explanation:**
- `counter()` = `10` (first call returns `n`)
- `counter()` = `11` (returns `1` more than the previous call)
- `counter()` = `12` (returns `1` more than the previous call)
- `counter()` initially returns `-2` and increments with each subsequent call.

## Platform : [LeetCode](https://leetcode.com/problems/counter)
## Solution Approach
The problem is solved using **closures** in JavaScript:
- Define a function `createCounter(n)` that takes `n` as input.
- Inside `createCounter(n)`, return a nested function that retains access to `n`.
- Each time the nested function is called, it returns `n` and increments it (`n++`).
- The function uses **closure** to maintain the state of `n` across multiple calls.

## Code
```javascript
/**
 * @param {number} n
 * @return {Function} counter
 */
var createCounter = function(n) {
    return function() {
        return n++;
    };
};

/** 
 * Example usage:
 * const counter = createCounter(10);
 * console.log(counter()); // 10
 * console.log(counter()); // 11
 * console.log(counter()); // 12
 */
```
