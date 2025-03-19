# To Be or Not To Be

## Problem
Write a function `expect` that helps developers test their code. It should take in any value `val` and return an object with the following two functions:

- `toBe(val)`: Accepts another value and returns `true` if the two values are strictly equal (`===`). If they are not equal, it should throw an error `"Not Equal"`.
- `notToBe(val)`: Accepts another value and returns `true` if the two values are **not** strictly equal (`!==`). If they are equal, it should throw an error `"Equal"`.

### Example 1:

| Example | Input                                | Output                 |
| ------- | ------------------------------------ | ---------------------- |
| 1       | func = () => expect(5).toBe(5)       | {"value": true}        |
| 2       | func = () => expect(5).toBe(null)    | {"error": "Not Equal"} |
| 3       | func = () => expect(5).notToBe(null) | {"value": true}        |

**Explanation:**
- `5 === 5`, so this expression returns `true`.

- `5 !== null`, so this expression throws the error `"Not Equal"`.

`5 !== null`, so this expression returns `true`.

## Platform : [LeetCode](https://leetcode.com/problems/to-be-or-not-to-be)

## Solution Approach
- The `expect` function takes an input value `val`.
- It returns an object with two methods:
  - `toBe(compareVal)`: Checks if `val === compareVal`. If true, returns `true`. Otherwise, throws `"Not Equal"`.
  - `notToBe(compareVal)`: Checks if `val !== compareVal`. If true, returns `true`. Otherwise, throws `"Equal"`.
- This solution demonstrates **closures** and **method chaining** in JavaScript.

## Code
```javascript
var expect = function(val) {
    return {
        toBe: function(compareVal) {
            if (val === compareVal) {
                return true;
            }
            throw new Error("Not Equal");
        },
        notToBe: function(compareVal) {
            if (val !== compareVal) {
                return true;
            }
            throw new Error("Equal");
        }
    };
};

```

