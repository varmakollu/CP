# Hello World Function

## Problem
Write a function `createHelloWorld`. It should return a new function that always returns `"Hello World"`.

### Examples
| S.No | Input                 | Output        | Explanation                                                      |
| ---- | --------------------- | ------------- | ---------------------------------------------------------------- |
| 1    | args = []             | "Hello World" | const f = createHelloWorld();
|      |                       |               |     f(); // "Hello World"             |
| 2    | args = [{}, null, 42] | "Hello World" | const f = createHelloWorld(); |
|      |                       |            | f({}, null, 42); // "Hello World" <br> |

- The function returned by `createHelloWorld` should always return `"Hello World"`.
- Any arguments could be passed to the function, but it should still always return `"Hello World"`.

## Constraints
- `0 <= args.length <= 10`

## Platform : [LeetCode](https://leetcode.com/problems/create-hello-world-function)

## Solution Approach
The problem is solved using **closures** in JavaScript:
- Define a function `createHelloWorld()` that returns a new function.
- The returned function accepts any number of arguments but always returns `"Hello World"`.
- This demonstrates the concept of **function factories** and closures.

## Code
```javascript
var createHelloWorld = function() {
    return function() {
        return "Hello World";
    };
};

```

