# ASCII Square Generator

## Problem Statement
The goal of this program is to generate a square using ASCII characters based on an integer input. The square should be drawn using the following symbols:

- `+` for the corners
- `-` for the top and bottom edges
- `|` for the left and right edges
- Spaces (` `) for the interior

## Platform : [Kattis](https://open.kattis.com/problems/asciikassi)

## Input Format
- The input consists of a single integer `n` representing the interior side length of the square.
- The value of `n` determines the number of spaces inside the square.

## Output Format
- The output is a square of size `(n+2) x (n+2)`, following the constraints:
  - The first and last rows contain `+` at both ends and `-` in between.
  - The middle `n` rows contain `|` at both ends with `n` spaces in between.

## Constraints
- `0 ≤ n ≤ 80`
- The output should have exactly the correct number of spaces. Any extra or missing space will lead to incorrect results.

## Sample Test Cases

### **Input 1**
```
0
```
### **Output 1**
```
++
++
```
---

## Implementation
This problem has been implemented in both **C** and **Python**.

### **C Implementation**
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    // Print the top border
    printf("+");
    for (int i = 0; i < n; i++) printf("-");
    printf("+\n");

    // Print the middle part
    for (int i = 0; i < n; i++) {
        printf("|");
        for (int j = 0; j < n; j++) printf(" ");
        printf("|\n");
    }

    // Print the bottom border
    printf("+");
    for (int i = 0; i < n; i++) printf("-");
    printf("+\n");

    return 0;
}
```

---

### **Python Implementation**
```python
n = int(input())

# Print the top border
print("+" + "-" * n + "+")

# Print the middle part
for _ in range(n):
    print("|" + " " * n + "|")

# Print the bottom border
print("+" + "-" * n + "+")
```
